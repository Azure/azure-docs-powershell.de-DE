---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: 3ffc76c06a5d34a702c6a6856469e352a683fe14
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289757"
---
# Get-AzVMDscExtensionStatus

## SYNOPSIS
Ruft den Status des DSC-Erweiterungshandlers für einen virtuellen Computer ab.

## SYNTAX

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzVMDscExtensionStatus"** ruft den Status des Erweiterungshandlers (Desired State Configuration, DSC) für einen virtuellen Computer in einer Ressourcengruppe ab.
Wenn eine Konfiguration angewendet wird, erzeugt dieses Cmdlet eine Ausgabe, die dem Start-DscConfiguration entspricht.

## BEISPIELE

### Beispiel 1

Ruft den Status des DSC-Erweiterungshandlers für einen virtuellen Computer ab. (automatisch generiert)

```powershell <!-- Aladdin Generated Example --> 
Get-AzVMDscExtensionStatus -Name 'AgentPool01' -ResourceGroupName myresourcegroup -VMName 'VM01'
```

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
Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.
Das Set-AzVMDscExtension-Cmdlet legt diesen Namen auf "Microsoft.Powershell.DSC" fest. Dies ist der gleiche Wert, der von **"Get-AzVMDscExtensionStatus" verwendet wird.**
Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Cmdlet "Set" geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des virtuellen Computers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet den Status der DSC-Erweiterung erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


