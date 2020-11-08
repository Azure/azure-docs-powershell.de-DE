---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f91747d7c48521a9a14906cd873df564fadc4aa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010468"
---
# Remove-AzSpringCloudAppDeployment

## Synopsis
Vorgang zum Löschen einer Bereitstellung.

## Syntax

### Löschen (Standard)
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Vorgang zum Löschen einer Bereitstellung.

## Beispiele

### Beispiel 1: Entfernen Sie die Bereitstellung der Feder Wolke nach Namen.
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

Entfernen Sie die Bereitstellung der Quell Wolke nach Namen.

### Beispiel 2: Entfernen der Bereitstellung für die Quell Wolke aus Pipe
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

Entfernen Sie die Bereitstellung der Quell Wolke aus Pipe.

## Parameter

### -AppName
Der Name der APP-Ressource.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name der Bereitstellungs Ressource.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt "true" zurück, wenn der Befehl erfolgreich ist

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe, die die Ressource enthält.
Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Der Name der Dienstressource.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnement-Nr
Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.
Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity

## Ausgaben

### System. Boolean

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Inputobject <ISpringCloudIdentity> : Identity-Parameter
  - `[AppName <String>]`: Der Name der APP-Ressource.
  - `[BindingName <String>]`: Der Name der Bindungs Ressource.
  - `[CertificateName <String>]`: Der Name der Zertifikat Ressource.
  - `[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.
  - `[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[Location <String>]`: die Region
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.
  - `[ServiceName <String>]`: Der Name der Dienstressource.
  - `[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

## Verwandte Links

