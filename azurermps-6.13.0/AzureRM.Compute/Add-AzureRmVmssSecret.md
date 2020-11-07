---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 423cb695e4dedb978c3902e9c2f2c891a977464c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662190"
---
# Add-AzureRmVmssSecret

## Synopsis
Fügt einen Schlüssel zu einem VMSS hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das **Add-AzureRmVmssSecret-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) einen Schlüssel hinzu.
Der Schlüssel muss in einem Azure Key Vault gespeichert werden.
Weitere Informationen zu Key Vault finden Sie unter [Was ist Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault-Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) in der Microsoft Developer-Netzwerkbibliothek oder im Cmdlet " [AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) ".

## Beispiele

### Beispiel 1: Hinzufügen eines Geheimnisses zum VMSS
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

In diesem Beispiel wird der VMSS ein Schlüssel hinzugefügt.
Der erste Befehl verwendet das Get-AzureRmKeyVault-Cmdlet, um einen Vault Secret aus dem Vault mit dem Namen ContosoVault abzurufen, und speichert das Ergebnis in der Variablen mit dem Namen $Vault.
Der zweite Befehl verwendet das Cmdlet **New-AzureRmVmssVaultCertificateConfig** zum Erstellen einer Schlüsseldepot-Zertifikatkonfiguration unter Verwendung der angegebenen Zertifikat-URL aus dem Zertifikatspeicher mit dem Namen Zertifikate und speichert die Ergebnisse in der Variablen mit dem Namen $CertConfig.
Der dritte Befehl verwendet das Cmdlet **New-AzureRmVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.
Der vierte Befehl fügt dem VMSS mithilfe der Schlüsselressourcen-ID und des Vault-Zertifikats, das in den $Vault-und $CertConfig Variablen gespeichert ist, einen geheimen Schlüssel hinzu.

## Parameter

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
Sie können das Cmdlet [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) verwenden, um dieses Objekt zu erstellen.

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
Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um dieses Objekt zu erstellen.

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

[Neu – AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md)

[Neu – AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
