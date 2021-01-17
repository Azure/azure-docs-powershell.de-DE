---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363948"
---
# Get-AzRecoveryServicesVault

## SYNOPSIS

Ruft eine Liste der Wiederherstellungsdienste-Tresore ab.

## SYNTAX

### ByTagNameValueParameterSet
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTagObjectParameterSet
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG

Das **Cmdlet "Get-AzRecoveryServicesVault"** ruft eine Liste der Recovery Services-Tresore im aktuellen Abonnement ab.

## BEISPIELE

### Beispiel 1

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

Holen Sie sich die Liste des Tresors im ausgewählten Abonnement.

### Beispiel 2

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

Holen Sie sich die Liste des Tresors in der Ressourcengruppe im ausgewählten Abonnement.

### Beispiel 3

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

Holen Sie sich den Tresor in der Ressourcengruppe mit dem angegebenen Namen.

## PARAMETERS

### -DefaultProfile

Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

Gibt den Namen des Tresors an, nach dem eine Abfrage ausgeführt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName

Gibt den Namen der Azure-Ressourcengruppe an, aus der das angegebene Wiederherstellungsdienstobjekt abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag

Gibt die Tags an, die abgefragt werden müssen

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagName

Gibt den Schlüssel des tags an, für den eine Abfrage ausgeführt werden soll.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagValue

Gibt den Wert des Tags an, für das eine Abfrage ausgeführt werden soll.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## HINWEISE
Get-AzRecoveryServicesVault in der alten Version von Az.RecoveryServices(<=2.10.0) kann mit Az.Accounts(>=1.8.1) aufgrund eines falschen Assemblyverweises nicht verwendet werden. Das Modul Az.RecoveryServices muss auf 2.11.0 oder neuer aktualisiert werden, wenn Sie die neuesten Az- oder Az.-Konten verwenden.

## LINKS ZU VERWANDTEN THEMEN

[Get-AzRecoveryServicesVaultSettingsFile](./Get-AzRecoveryServicesVaultSettingsFile.md)

[New-AzRecoveryServicesVault](./New-AzRecoveryServicesVault.md)

[Remove-AzRecoveryServicesVault](./Remove-AzRecoveryServicesVault.md)
