---
title: Verwalten von Azure-Ressourcen mit Invoke-AzRestMethod
description: Hier erfahren Sie, wie Sie Azure PowerShell zum Verwalten von Ressourcen mit dem Cmdlet „Invoke-AzRestMethod“ verwenden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 55d7cc06178257a9288e2d27f810d1180369ddc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753695"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>Verwalten von Azure-Ressourcen mit Invoke-AzRestMethod

[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) ist ein Azure PowerShell-Cmdlet, das in Version 4.4.0 des Az PowerShell-Moduls eingeführt wurde. Mit diesem Cmdlet können Sie benutzerdefinierte HTTP-Anforderungen unter Verwendung des Az-Kontexts an den ARM-Endpunkt (Azure Resource Manager) senden.

Dieses Cmdlet ist nützlich, wenn Sie Azure-Dienste im Hinblick auf Features verwalten möchten, die im Az PowerShell-Modul noch nicht verfügbar sind.

## <a name="how-to-use-invoke-azrestmethod"></a>Verwenden von „Invoke-AzRestMethod“

Sie können beispielsweise Zugriff auf Azure Container Registry (ACR) ausschließlich für bestimmte Netzwerke zulassen oder den öffentlichen Zugriff verweigern. Ab Version 4.5.0 des Az PowerShell-Moduls ist dieses Feature im [PowerShell-Modul „Az.ContainerRegistry“](/powershell/module/Az.ContainerRegistry/) noch nicht verfügbar. Es kann in der Zwischenzeit jedoch mit `Invoke-AzRestMethod` verwaltet werden.

## <a name="using-invoke-azrestmethod-with-get-operations"></a>Verwenden von „Invoke-AzRestMethod“ mit GET-Vorgängen

Im folgenden Beispiel wird die Verwendung des Cmdlets `Invoke-AzRestMethod` in Verbindung mit einem GET-Vorgang veranschaulicht:

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

Um maximale Flexibilität zu ermöglichen, ist der Großteil der Parameter für `Invoke-AzRestMethod` optional.
Wenn Sie jedoch Ressourcen innerhalb einer Ressourcengruppe verwalten, müssen Sie wahrscheinlich entweder die vollständige ID für die Ressource oder Parameter wie Ressourcengruppe, Ressourcenanbieter und Ressourcentyp angeben.

Die Parameter `ResourceType` und `Name` können bei Ressourcen, die mehr als einen Namen erfordern, mehrere Werte annehmen. Zum Bearbeiten einer gespeicherten Suche in einem Log Analytics-Arbeitsbereich sehen die Parameter etwa wie im folgenden Beispiel aus: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.

Das Cmdlet erstellt mithilfe einer Zuordnung, die auf der Position im Array basiert, die folgende Ressource: `Id:'/workspaces/my-la/savedsearches/my-search'`.

Mit dem Parameter `APIVersion` können Sie eine bestimmte API-Version (einschließlich Vorschauversionen) verwenden. Die unterstützten API-Versionen für Azure-Ressourcenanbieter finden Sie im GitHub-Repository [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).

Die Definition für die ACR-Version „2019-12-01-preview“ befindet sich an folgendem Speicherort: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).

## <a name="using-invoke-azrestmethod-with-patch-operations"></a>Verwenden von „Invoke-AzRestMethod“ mit PATCH-Vorgängen

Sie können den öffentlichen Zugriff auf die vorhandene ACR-Instanz `myacr` in der Ressourcengruppe `myresourcegroup` mithilfe des Cmdlets `Invoke-AzRestMethod` deaktivieren.

Wenn Sie den Zugriff auf das öffentliche Netzwerk deaktivieren möchten, senden Sie einen **PATCH** -Aufruf an die API, der den Wert des Parameters `publicNetwokAccess` wie im folgenden Beispiel gezeigt ändert:

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

Bei der Eigenschaft `Payload` handelt es sich um eine JSON-Zeichenfolge, die den Pfad der zu ändernden Eigenschaft zeigt.

Alle Parameter für diese API sind in der Datei **rest-api-spec** für diese API beschrieben.
Die spezifische Definition für den publicNetworkAccess-Parameter finden Sie in der [JSON-Datei der Containerregistrierung](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) für die Vorschauversion „2019-12-01“ der API.

Wenn Sie den Zugriff auf die Registrierung nur von einer bestimmten IP-Adresse aus zulassen möchten, muss die Nutzlast wie im folgenden Beispiel gezeigt geändert werden:

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a>Vergleich mit „Get-AzResource“, „New-AzResource“ und „Remove-AzResource“

Mit den `*-AzResource`-Cmdlets können Sie den REST-API-Aufruf an Azure anpassen, indem Sie den Ressourcentyp, die API-Version und die zu aktualisierenden Eigenschaften angeben. Die Eigenschaften müssen jedoch zuerst als `PSObject` erstellt werden. Dieser Vorgang erhöht die Komplexität und kann kompliziert werden.

Mit `Invoke-AzRestMethod` lassen sich Azure-Ressourcen einfach verwalten. Wie im vorherigen Beispiel gezeigt, können Sie eine JSON-Zeichenfolge erstellen und diese zum Anpassen des REST-API-Aufrufs verwenden, ohne vorab `PSObjects` erstellen zu müssen.

Wenn Sie bereits mit den `*-AzResource`-Cmdlets vertraut sind, können Sie sie weiterhin verwenden. Es ist nicht geplant, ihre Unterstützung einzustellen. Mit `Invoke-AzRestMethod` wurde dem Toolkit ein neues Cmdlet hinzugefügt.

## <a name="see-also"></a>Weitere Informationen

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)
