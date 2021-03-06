---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: a2d9c59e3ff0b33ac6534d9f0c200b8fbc2eea44
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395219"
---
# Add-AzVmssSecret

## Synopsis
Fügt einen Schlüssel zu einem VMSS hinzu.

## Syntax

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das **Add-AzVmssSecret-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) einen Schlüssel hinzu.
Der Schlüssel muss in einem Azure Key Vault gespeichert werden.
Weitere Informationen zu Key Vault finden Sie unter [Was ist Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault-Cmdlets](/powershell/module/az.keyvault) oder dem Cmdlet " [AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) ".

## Beispiele

### Beispiel 1: Hinzufügen eines Geheimnisses zum VMSS
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

In diesem Beispiel wird der VMSS ein Schlüssel hinzugefügt.
Der erste Befehl verwendet das Get-AzKeyVault-Cmdlet, um einen Vault Secret aus dem Vault mit dem Namen ContosoVault abzurufen, und speichert das Ergebnis in der Variablen mit dem Namen $Vault.
Der zweite Befehl verwendet das Cmdlet **New-AzVmssVaultCertificateConfig** zum Erstellen einer Schlüsseldepot-Zertifikatkonfiguration unter Verwendung der angegebenen Zertifikat-URL aus dem Zertifikatspeicher mit dem Namen Zertifikate und speichert die Ergebnisse in der Variablen mit dem Namen $CertConfig.
Der dritte Befehl verwendet das Cmdlet **New-AzVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.
Der vierte Befehl fügt dem VMSS mithilfe der Schlüsselressourcen-ID und des Vault-Zertifikats, das in den $Vault-und $CertConfig Variablen gespeichert ist, einen geheimen Schlüssel hinzu.

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

### -SourceVaultId
Gibt die Ressourcen-ID des Schlüsseldepots an, das die Zertifikate enthält, die Sie dem virtuellen Computer hinzufügen können.
Dieser Wert fungiert auch als Schlüssel zum Hinzufügen mehrerer Zertifikate.
Das bedeutet, dass Sie für den *SourceVaultId* -Parameter denselben Wert verwenden können, wenn Sie mehrere Zertifikate aus demselben Schlüsselspeicher hinzufügen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultCertificate
Gibt das Vault **Certificate** -Objekt an, das die Zertifikat-URL und den Zertifikatsnamen enthält.
Sie können das Cmdlet [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) verwenden, um dieses Objekt zu erstellen.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Gibt das VMSS-Objekt an.
Sie können das Cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um dieses Objekt zu erstellen.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

### System. String

### Microsoft. Azure. Management. Compute. Models. VaultCertificate []

## Ausgaben

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## Notizen

## Verwandte Links

[Neu – AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md)

[Neu – AzVmssConfig](./New-AzVmssConfig.md)
