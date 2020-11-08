---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 1f0f3a9986f69be082a91606d07e86d493f4a269
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173125"
---
# <span data-ttu-id="cc133-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cc133-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="cc133-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc133-102">SYNOPSIS</span></span>
<span data-ttu-id="cc133-103">Löscht eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="cc133-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="cc133-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc133-104">SYNTAX</span></span>

### <span data-ttu-id="cc133-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc133-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc133-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc133-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc133-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cc133-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc133-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc133-108">DESCRIPTION</span></span>
<span data-ttu-id="cc133-109">Das Remove-AzPowerBIEmbeddedCapacity-Cmdlet löscht eine Instanz der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="cc133-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="cc133-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc133-110">EXAMPLES</span></span>

### <span data-ttu-id="cc133-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc133-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="cc133-112">Dieser Befehl entfernt die Kapazität mit dem Namen testcapacity in der testRG</span><span class="sxs-lookup"><span data-stu-id="cc133-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="cc133-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc133-113">PARAMETERS</span></span>

### <span data-ttu-id="cc133-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc133-114">-DefaultProfile</span></span>
<span data-ttu-id="cc133-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc133-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc133-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc133-116">-InputObject</span></span>
<span data-ttu-id="cc133-117">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="cc133-117">Input object for Piping</span></span>

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

### <span data-ttu-id="cc133-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cc133-118">-Name</span></span>
<span data-ttu-id="cc133-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="cc133-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="cc133-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc133-120">-PassThru</span></span>
<span data-ttu-id="cc133-121">Gibt die gelöschten Kapazitätsdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc133-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="cc133-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc133-122">-ResourceGroupName</span></span>
<span data-ttu-id="cc133-123">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="cc133-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="cc133-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cc133-124">-ResourceId</span></span>
<span data-ttu-id="cc133-125">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="cc133-125">Azure resource ID</span></span>

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

### <span data-ttu-id="cc133-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc133-126">-Confirm</span></span>
<span data-ttu-id="cc133-127">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="cc133-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="cc133-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc133-128">-WhatIf</span></span>
<span data-ttu-id="cc133-129">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="cc133-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="cc133-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc133-130">CommonParameters</span></span>
<span data-ttu-id="cc133-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc133-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc133-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc133-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc133-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc133-133">INPUTS</span></span>

### <span data-ttu-id="cc133-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cc133-134">System.String</span></span>

### <span data-ttu-id="cc133-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cc133-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="cc133-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc133-136">OUTPUTS</span></span>

### <span data-ttu-id="cc133-137">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cc133-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="cc133-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc133-138">NOTES</span></span>

## <span data-ttu-id="cc133-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc133-139">RELATED LINKS</span></span>

[<span data-ttu-id="cc133-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cc133-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="cc133-141">Neu – AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cc133-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
