---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fe660d200c578d15fe8e23e7bfffc9a249651ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476713"
---
# <span data-ttu-id="ab91e-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ab91e-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="ab91e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab91e-102">SYNOPSIS</span></span>
<span data-ttu-id="ab91e-103">Setzt eine Instanz der eingebetteten PowerBI-Kapazität fort.</span><span class="sxs-lookup"><span data-stu-id="ab91e-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab91e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab91e-104">SYNTAX</span></span>

```
Resume-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="ab91e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab91e-105">DESCRIPTION</span></span>
<span data-ttu-id="ab91e-106">Das Resume-AzureRmPowerBIEmbeddedCapacity-Cmdlet setzt eine Instanz der eingebetteten PowerBI-Kapazität fort</span><span class="sxs-lookup"><span data-stu-id="ab91e-106">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="ab91e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab91e-107">EXAMPLES</span></span>

### <span data-ttu-id="ab91e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ab91e-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="ab91e-109">Dieser Befehl setzt eine angehaltene Kapazität mit dem Namen testcapacity in der testRG</span><span class="sxs-lookup"><span data-stu-id="ab91e-109">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="ab91e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab91e-110">PARAMETERS</span></span>

### <span data-ttu-id="ab91e-111">-Name</span><span class="sxs-lookup"><span data-stu-id="ab91e-111">-Name</span></span>
<span data-ttu-id="ab91e-112">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="ab91e-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="ab91e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab91e-113">-ResourceGroupName</span></span>
<span data-ttu-id="ab91e-114">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="ab91e-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="ab91e-115">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ab91e-115">-ResourceId</span></span>
<span data-ttu-id="ab91e-116">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ab91e-116">Azure resource ID</span></span>

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

### <span data-ttu-id="ab91e-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab91e-117">-InputObject</span></span>
<span data-ttu-id="ab91e-118">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="ab91e-118">Input object for Piping</span></span>

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

### <span data-ttu-id="ab91e-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab91e-119">-Confirm</span></span>
<span data-ttu-id="ab91e-120">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="ab91e-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="ab91e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab91e-121">-WhatIf</span></span>
<span data-ttu-id="ab91e-122">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="ab91e-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="ab91e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab91e-123">CommonParameters</span></span>
<span data-ttu-id="ab91e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab91e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab91e-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab91e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab91e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab91e-126">INPUTS</span></span>

### <span data-ttu-id="ab91e-127">Keine</span><span class="sxs-lookup"><span data-stu-id="ab91e-127">None</span></span>
<span data-ttu-id="ab91e-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ab91e-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab91e-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab91e-129">OUTPUTS</span></span>

### <span data-ttu-id="ab91e-130">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ab91e-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="ab91e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab91e-131">NOTES</span></span>

## <span data-ttu-id="ab91e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab91e-132">RELATED LINKS</span></span>

[<span data-ttu-id="ab91e-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ab91e-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="ab91e-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ab91e-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
