---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bbdfe43b4f6cad72432c85876c71bcd34a9a371c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663460"
---
# <span data-ttu-id="173b8-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="173b8-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="173b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="173b8-102">SYNOPSIS</span></span>
<span data-ttu-id="173b8-103">Löscht eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="173b8-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="173b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="173b8-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="173b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="173b8-105">DESCRIPTION</span></span>
<span data-ttu-id="173b8-106">Das Remove-AzureRmPowerBIEmbeddedCapacity-Cmdlet löscht eine Instanz der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="173b8-106">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="173b8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="173b8-107">EXAMPLES</span></span>

### <span data-ttu-id="173b8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="173b8-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

```

<span data-ttu-id="173b8-109">Dieser Befehl entfernt die Kapazität mit dem Namen testcapacity in der testRG</span><span class="sxs-lookup"><span data-stu-id="173b8-109">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="173b8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="173b8-110">PARAMETERS</span></span>

### <span data-ttu-id="173b8-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="173b8-111">-ResourceGroupName</span></span>
<span data-ttu-id="173b8-112">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="173b8-112">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="173b8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="173b8-113">-Name</span></span>
<span data-ttu-id="173b8-114">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="173b8-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="173b8-115">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="173b8-115">-ResourceId</span></span>
<span data-ttu-id="173b8-116">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="173b8-116">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="173b8-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="173b8-117">-InputObject</span></span>
<span data-ttu-id="173b8-118">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="173b8-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="173b8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="173b8-119">-PassThru</span></span>
<span data-ttu-id="173b8-120">Gibt die gelöschten Kapazitätsdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="173b8-120">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="173b8-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="173b8-121">-Confirm</span></span>
<span data-ttu-id="173b8-122">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="173b8-122">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="173b8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="173b8-123">-WhatIf</span></span>
<span data-ttu-id="173b8-124">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="173b8-124">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="173b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="173b8-125">CommonParameters</span></span>
<span data-ttu-id="173b8-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="173b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="173b8-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="173b8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="173b8-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="173b8-128">INPUTS</span></span>

### <span data-ttu-id="173b8-129">Keine</span><span class="sxs-lookup"><span data-stu-id="173b8-129">None</span></span>
<span data-ttu-id="173b8-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="173b8-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="173b8-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="173b8-131">OUTPUTS</span></span>

### <span data-ttu-id="173b8-132">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="173b8-132">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="173b8-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="173b8-133">NOTES</span></span>

## <span data-ttu-id="173b8-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="173b8-134">RELATED LINKS</span></span>

[<span data-ttu-id="173b8-135">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="173b8-135">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="173b8-136">Neu – AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="173b8-136">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
