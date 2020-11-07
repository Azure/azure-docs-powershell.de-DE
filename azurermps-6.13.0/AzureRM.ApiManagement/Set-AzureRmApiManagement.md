---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663705"
---
# Set-AzureRmApiManagement

## Synopsis
Aktualisiert einen Azure API-Verwaltungsdienst

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung

Das Cmdlet " **Satz-AzureRmApiManagement** " aktualisiert einen Azure API-Verwaltungsdienst.

## Beispiele

### Beispiel 1 Abrufen eines API-Verwaltungsdiensts und Skalieren auf Premium und Hinzufügen eines Bereichs
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

In diesem Beispiel wird eine API-Verwaltungsinstanz abgerufen, auf fünf Premium-Einheiten skaliert und dann dem Premium-Bereich weitere drei Einheiten hinzugefügt.

### Beispiel 2: Update Bereitstellung (externe VNET)
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

Mit diesem Befehl wird eine vorhandene API-Verwaltungs Bereitstellung aktualisiert und eine Verknüpfung zu einem externen *VpnType*.

### Beispiel 3: Erstellen und Initialisieren einer Instanz von PsApiManagementCustomHostNameConfiguration mit einem Schlüssel aus der keyvault-Ressource
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

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

### -AssignIdentity
Sie können eine Azure Active Directory-Identität für diesen Server für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault generieren und zuweisen.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Die ApiManagement-Instanz.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Sendet aktualisierte PsApiManagement an Pipeline, wenn der Vorgang erfolgreich ausgeführt wurde.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement
Parameter: Inputobject (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Notizen

## Verwandte Links

[Get-AzureRmApiManagement](./Get-AzureRmApiManagement.md)

[Neu – AzureRmApiManagement](./New-AzureRmApiManagement.md)

[Remove-AzureRmApiManagement](./Remove-AzureRmApiManagement.md)
