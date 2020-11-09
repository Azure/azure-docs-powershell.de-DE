---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296445"
---
# Update-AzDiskEncryptionSet

## Synopsis
Aktualisiert einen Datenträger Verschlüsselungs Satz.

## Syntax

### Defaultparameter (Standard)
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ResourceIdParameter
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ObjectParameter
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Aktualisiert einen Datenträger Verschlüsselungs Satz.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

Aktualisiert den Datenträger Verschlüsselungs Satz mithilfe des angegebenen aktiven Schlüssels im Schlüsselspeicher.

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

### -Inputobject
Das lokale Objekt des Datenträger Verschlüsselungs Satzes.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyUrl
URL, der auf den aktiven Schlüssel in keyvault zeigt

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Name des Festplatten-Verschlüsselungs Satzes.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Die ID der Ressource.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceVaultId
Die Ressourcen-ID des keyvaults mit dem aktiven Schlüssel.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

### System. String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet

### System. Collections. Hashtable

## Ausgaben

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet

## Notizen

## Verwandte Links
