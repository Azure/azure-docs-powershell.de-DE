---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503909"
---
# New-AzureRmApiManagement

## Synopsis
Erstellt eine API-Verwaltungs Bereitstellung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmApiManagement** erstellt eine API-Verwaltungs Bereitstellung in Azure API-Verwaltung.

## Beispiele

### Beispiel 1: Erstellen eines API-Verwaltungsdiensts für die Entwicklerebene
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

Dieser Befehl erstellt einen API-Verwaltungsdienst für Entwickler Ebenen.
Der Befehl gibt die Organisation und die Administratoradresse an.
Der Befehl gibt den *SKU* -Parameter nicht an.
Daher verwendet das Cmdlet den Standardwert von Developer.

### Beispiel 2: Erstellen eines Standard Tier Diensts mit drei Einheiten
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

Mit diesem Befehl wird ein Standard-Tier-API-Verwaltungsdienst mit drei Einheiten erstellt.

### Beispiel 3: Erstellen eines API-Verwaltungsdiensts für ein externes virtuelles Netzwerk
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

Dieser Befehl erstellt einen Premium-Tier-API-Verwaltungsdienst in einem Azure Virtual Network-Subnetz mit einem extern zugewandten Gateway-Endpunkt mit einem Masterbereich im Westen der USA.

### Beispiel 4: Erstellen eines API-Verwaltungsdiensts für ein internes virtuelles Netzwerk
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

Dieser Befehl erstellt einen Premium-Tier-API-Verwaltungsdienst in einem Azure Virtual Network-Subnetz mit einem internen Gateway-Endpunkt mit einem Masterbereich im Westen der USA.

## Parameter

### -AdditionalRegions
Zusätzliche Bereitstellungsbereiche der Azure-API-Verwaltung.

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminEmail
Gibt die ursprüngliche e-Mail-Adresse für alle Benachrichtigungen an, die vom API-Verwaltungssystem gesendet werden.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kapazität
Gibt die SKU-Kapazität des Azure API-Verwaltungsdiensts an.
Der Standardwert ist eins (1).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Gibt den Speicherort an, an dem der API-Verwaltungsdienst erstellt werden soll.

Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für die API-Verwaltungs Bereitstellung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Organisation
Gibt den Namen einer Organisation an.
Die API-Verwaltung verwendet diese Adresse im Entwicklerportal in e-Mail-Benachrichtigungen.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet eine API-Verwaltungs Bereitstellung erstellt.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Gibt die Stufe des API-Verwaltungsdiensts an.
Gültige Werte sind: 

- Entwickler 
- Standard 
- Premium 

Der Standardwert ist Developer.

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Tags-Wörterbuch.

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Konfiguration des virtuellen Netzwerks des Master Azure API Management Deployment-Bereichs.

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnType
Virtueller Netzwerktyp der ApiManagement-Bereitstellung. Gültige Werte sind 
- "None" (Standardwert. ApiManagement ist nicht Bestandteileines virtuellen Netzwerks ")
- "Extern" (ApiManagement-Bereitstellung erfolgt in einem virtuellen Netzwerk mit einem Internet-Endpunkt)
- "Intern" (ApiManagement-Bereitstellung erfolgt in einem virtuellen Netzwerk mit einem Intranet-Endpunkt)

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Notizen

## Verwandte Links

[Backup-AzureRmApiManagement](./Backup-AzureRmApiManagement.md)

[Get-AzureRmApiManagement](./Get-AzureRmApiManagement.md)

[Remove-AzureRmApiManagement](./Remove-AzureRmApiManagement.md)

[Wiederherstellen – AzureRmApiManagement](./Restore-AzureRmApiManagement.md)


