---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 18359b0086257719bc0d050629c532756634a89e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179383"
---
# <span data-ttu-id="05c25-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="05c25-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="05c25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05c25-102">SYNOPSIS</span></span>
<span data-ttu-id="05c25-103">Unterbricht eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="05c25-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="05c25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05c25-104">SYNTAX</span></span>

### <span data-ttu-id="05c25-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="05c25-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c25-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="05c25-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c25-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05c25-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05c25-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05c25-108">DESCRIPTION</span></span>
<span data-ttu-id="05c25-109">Das Suspend-AzPowerBIEmbeddedCapacity-Cmdlet unterbricht eine Instanz der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="05c25-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="05c25-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05c25-110">EXAMPLES</span></span>

### <span data-ttu-id="05c25-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05c25-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="05c25-112">Dieser Befehl unterbricht eine aktive Kapazität mit dem Namen "testcapacity" in der testgroup der ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="05c25-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="05c25-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="05c25-113">PARAMETERS</span></span>

### <span data-ttu-id="05c25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c25-114">-DefaultProfile</span></span>
<span data-ttu-id="05c25-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05c25-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05c25-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="05c25-116">-InputObject</span></span>
<span data-ttu-id="05c25-117">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="05c25-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05c25-118">-Name</span><span class="sxs-lookup"><span data-stu-id="05c25-118">-Name</span></span>
<span data-ttu-id="05c25-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="05c25-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c25-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05c25-120">-PassThru</span></span>
<span data-ttu-id="05c25-121">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="05c25-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="05c25-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c25-122">-ResourceGroupName</span></span>
<span data-ttu-id="05c25-123">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="05c25-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c25-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="05c25-124">-ResourceId</span></span>
<span data-ttu-id="05c25-125">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="05c25-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c25-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05c25-126">-Confirm</span></span>
<span data-ttu-id="05c25-127">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="05c25-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="05c25-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05c25-128">-WhatIf</span></span>
<span data-ttu-id="05c25-129">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="05c25-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="05c25-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c25-130">CommonParameters</span></span>
<span data-ttu-id="05c25-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05c25-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c25-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05c25-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c25-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05c25-133">INPUTS</span></span>

### <span data-ttu-id="05c25-134">System. String</span><span class="sxs-lookup"><span data-stu-id="05c25-134">System.String</span></span>

### <span data-ttu-id="05c25-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="05c25-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="05c25-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05c25-136">OUTPUTS</span></span>

### <span data-ttu-id="05c25-137">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="05c25-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="05c25-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="05c25-138">NOTES</span></span>

## <span data-ttu-id="05c25-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05c25-139">RELATED LINKS</span></span>

[<span data-ttu-id="05c25-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="05c25-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="05c25-141">Lebenslauf-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="05c25-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

