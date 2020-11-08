---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166344"
---
# <span data-ttu-id="8423b-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="8423b-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="8423b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8423b-102">SYNOPSIS</span></span>
<span data-ttu-id="8423b-103">Anwenden von Wartungsupdates auf die Ressource</span><span class="sxs-lookup"><span data-stu-id="8423b-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="8423b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8423b-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8423b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8423b-105">DESCRIPTION</span></span>
<span data-ttu-id="8423b-106">Anwenden von Wartungsupdates auf die Ressource</span><span class="sxs-lookup"><span data-stu-id="8423b-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="8423b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8423b-107">EXAMPLES</span></span>

### <span data-ttu-id="8423b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8423b-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="8423b-109">Anwenden von Wartungsupdates auf die Ressource</span><span class="sxs-lookup"><span data-stu-id="8423b-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="8423b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8423b-110">PARAMETERS</span></span>

### <span data-ttu-id="8423b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8423b-111">-AsJob</span></span>
<span data-ttu-id="8423b-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8423b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8423b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8423b-113">-DefaultProfile</span></span>
<span data-ttu-id="8423b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8423b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8423b-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="8423b-115">-ProviderName</span></span>
<span data-ttu-id="8423b-116">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="8423b-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="8423b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8423b-117">-ResourceGroupName</span></span>
<span data-ttu-id="8423b-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8423b-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="8423b-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8423b-119">-ResourceName</span></span>
<span data-ttu-id="8423b-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8423b-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8423b-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="8423b-121">-ResourceParentName</span></span>
<span data-ttu-id="8423b-122">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="8423b-122">The parent resource name.</span></span>

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

### <span data-ttu-id="8423b-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="8423b-123">-ResourceParentType</span></span>
<span data-ttu-id="8423b-124">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="8423b-124">The parent resource type.</span></span>

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

### <span data-ttu-id="8423b-125">-</span><span class="sxs-lookup"><span data-stu-id="8423b-125">-ResourceType</span></span>
<span data-ttu-id="8423b-126">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="8423b-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8423b-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8423b-127">-Confirm</span></span>
<span data-ttu-id="8423b-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8423b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8423b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8423b-129">-WhatIf</span></span>
<span data-ttu-id="8423b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8423b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8423b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8423b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8423b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8423b-132">CommonParameters</span></span>
<span data-ttu-id="8423b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8423b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8423b-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8423b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8423b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8423b-135">INPUTS</span></span>

### <span data-ttu-id="8423b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8423b-136">System.String</span></span>

## <span data-ttu-id="8423b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8423b-137">OUTPUTS</span></span>

### <span data-ttu-id="8423b-138">Microsoft. Azure. Commands. Maintenance. Models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="8423b-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="8423b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="8423b-139">NOTES</span></span>

## <span data-ttu-id="8423b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8423b-140">RELATED LINKS</span></span>
