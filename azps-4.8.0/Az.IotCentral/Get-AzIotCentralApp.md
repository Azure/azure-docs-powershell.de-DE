---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166909"
---
# Get-AzIotCentralApp

## Synopsis
Ruft Eigenschaften für eine oder mehrere zentrale Anwendungen ab.

## Syntax

### ListIotCentralAppsParameterSet (Standard)
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Ruft je nach Parameter Satz die Metadaten für eine bestimmte viel zentrale Anwendung oder alle Anwendungen in einer Ressourcengruppe oder einem Abonnement ab. 

## Beispiele

### Beispiel 1: Abrufen einer bestimmten zentralen Anwendung.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

Ruft die Metadaten für die angegebene viel zentrale Anwendung ab.

Beispielausgabe:

Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName-Name: MyAppResourceName-Typ: Microsoft. IoTCentral/IoTApps-Standort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-DisplayName-Unterdomäne für den benutzerdefinierten Anzeige Namen: MyAppSubdomain-Vorlage: xxxxxxxx iotc-default@1.0.0

### Beispiel 2: Abrufen von zentralen Anwendungen im Abonnement.
```powershell
PS C:\> Get-AzIotCentralApp
```

Ruft die Metadaten für alle zentralen Anwendungen im aktuellen Abonnement ab.

Beispielausgabe:

Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName-Name: MyAppResourceName-Typ: Microsoft. IoTCentral/IoTApps-Standort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-DisplayName-Unterdomäne für den benutzerdefinierten Anzeige Namen: MyAppSubdomain-Vorlage: xxxxxxxx iotc-default@1.0.0

Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName2/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2-Name: MyAppResourceName2-Typ: Microsoft. IoTCentral/IoTApps-Ort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: mein benutzerdefinierter Anzeige Name 2 Subdomain: MyAppSubdomain2 Vorlage: iotc-default@1.0.0 Abonnement-Nr: xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName2

### Beispiel 3: Abrufen von zentralen Anwendungen in der Ressourcengruppe.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

Ruft die Metadaten für alle zentralen Anwendungen in der bereitgestellten Ressourcengruppe ab.

Beispielausgabe:

Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName-Name: MyAppResourceName-Typ: Microsoft. IoTCentral/IoTApps-Standort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-DisplayName-Unterdomäne für den benutzerdefinierten Anzeige Namen: MyAppSubdomain-Vorlage: xxxxxxxx iotc-default@1.0.0

Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2-Name: MyAppResourceName2-Typ: Microsoft. IoTCentral/IoTApps-Ort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: mein benutzerdefinierter Anzeige Name 2 Subdomain: MyAppSubdomain2 Vorlage: iotc-default@1.0.0 Abonnement-Nr: xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der zentralen Anwendungsressource.

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Ressourcen-ID der zentralen Anwendung.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp

## Notizen

## Verwandte Links
