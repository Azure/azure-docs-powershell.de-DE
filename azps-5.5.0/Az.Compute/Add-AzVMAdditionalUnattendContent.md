---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171312"
---
# Add-AzVMAdditionalUnattendContent

## SYNOPSIS
Fügt der unbeaufsichtigten Antwortdatei für Windows Setup Informationen hinzu.

## SYNTAX

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzVMAdditionalUnattendContent"** fügt der unbeaufsichtigten Antwortdatei für Windows Setup Informationen hinzu.
Geben Sie zusätzliche, mit Basis 64 codierte XML-formatierte Informationen an, die dieses Cmdlet der unattend.xml hinzufügt.

## BEISPIELE

### Beispiel 1: Hinzufügen von Inhalt zu unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

Der erste Befehl ruft den Verfügbarkeitssatz namens "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variable.
Der zweite Befehl erstellt ein Objekt des virtuellen Computers und speichert es dann in der $VirtualMachine Variable.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.
Der dritte Befehl erstellt mithilfe des Cmdlets "Get-Credential" ein Anmeldeinformationsobjekt und speichert das Ergebnis dann in der $Credential Variable.
Der Befehl fordert Sie zur Eingabe eines Benutzernamens und Kennworts auf.
Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Credential` eingeben" aus.
Der vierte Befehl verwendet das **Cmdlet "Set-AzVMOperatingSystem",** um den virtuellen Computer zu konfigurieren, der in $VirtualMachine.
Der fünfte Befehl weist der Variablen $AucContent zu.
Der Inhalt enthält ein Kennwort.
Der letzte Befehl fügt den in der Datei gespeicherten $AucContent der unattend.xml hinzu.

## PARAMETERS

### -Content
Gibt den mit Basis 64 codierten XML-formatierten Inhalt an.
Dieses Cmdlet fügt den Inhalt der unattend.xml hinzu.
Der Inhalt des XML muss kleiner als 4 KB sein und muss das Stammelement für die Einstellung oder das Feature enthalten, die bzw. das von diesem Cmdlet eingefügt wird.

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

### -SettingName
Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.
Die zulässigen Werte für diesen Parameter sind:
- FirstLogonCommands
- AutoLogon

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.
Verwenden Sie das [Get-AzVM-Cmdlet,](./Get-AzVM.md) um ein Objekt des virtuellen Computers zu erhalten.
Erstellen Sie ein Objekt für einen virtuellen Computer mithilfe des [Cmdlets "New-AzVMConfig".](./New-AzVMConfig.md)

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[New-AzVMConfig](./New-AzVMConfig.md)
