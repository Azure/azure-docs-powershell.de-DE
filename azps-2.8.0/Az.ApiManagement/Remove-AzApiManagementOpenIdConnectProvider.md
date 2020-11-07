---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f148f65a6065040a28f936a5dec64f09ff4045eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658187"
---
# Remove-AzApiManagementOpenIdConnectProvider

## Synopsis
Entfernt einen OpenID Connect-Anbieter.

## Syntax

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzApiManagementOpenIdConnectProvider** entfernt einen OpenID Connect-Anbieter für die Azure-API-Verwaltung.

## Beispiele

### Beispiel 1: Entfernen eines Anbieters
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

Dieser Befehl entfernt einen Anbieter mit der ID OICProvider01.

## Parameter

### -Context
Gibt ein **PsApiManagementContext** -Objekt an.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

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

### -OpenIdConnectProviderId
Gibt eine ID des Anbieters an, den dieses Cmdlet entfernt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext

### System. String

### System. Management. Automation. Switchparameter

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Get-AzApiManagementOpenIdConnectProvider](./Get-AzApiManagementOpenIdConnectProvider.md)

[Neu – AzApiManagementOpenIdConnectProvider](./New-AzApiManagementOpenIdConnectProvider.md)

[Satz-AzApiManagementOpenIdConnectProvider](./Set-AzApiManagementOpenIdConnectProvider.md)


