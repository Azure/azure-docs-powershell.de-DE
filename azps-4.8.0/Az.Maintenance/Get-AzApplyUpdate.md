---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166359"
---
# <span data-ttu-id="48e2f-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="48e2f-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="48e2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="48e2f-103">Nachvollziehen von Wartungsupdates für die Ressource</span><span class="sxs-lookup"><span data-stu-id="48e2f-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="48e2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48e2f-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48e2f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48e2f-105">DESCRIPTION</span></span>
<span data-ttu-id="48e2f-106">Nachvollziehen von Wartungsupdates für die Ressource</span><span class="sxs-lookup"><span data-stu-id="48e2f-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="48e2f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48e2f-107">EXAMPLES</span></span>

### <span data-ttu-id="48e2f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48e2f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="48e2f-109">Nachvollziehen von Wartungsupdates für die Ressource</span><span class="sxs-lookup"><span data-stu-id="48e2f-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="48e2f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="48e2f-110">PARAMETERS</span></span>

### <span data-ttu-id="48e2f-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="48e2f-111">-ApplyUpdateName</span></span>
<span data-ttu-id="48e2f-112">Der Name der Aktualisierungs Ressource wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="48e2f-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e2f-113">-DefaultProfile</span></span>
<span data-ttu-id="48e2f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="48e2f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48e2f-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="48e2f-115">-ProviderName</span></span>
<span data-ttu-id="48e2f-116">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="48e2f-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="48e2f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e2f-117">-ResourceGroupName</span></span>
<span data-ttu-id="48e2f-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="48e2f-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="48e2f-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="48e2f-119">-ResourceName</span></span>
<span data-ttu-id="48e2f-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="48e2f-120">The resource name.</span></span>

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

### <span data-ttu-id="48e2f-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="48e2f-121">-ResourceParentName</span></span>
<span data-ttu-id="48e2f-122">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="48e2f-122">The parent resource name.</span></span>

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

### <span data-ttu-id="48e2f-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="48e2f-123">-ResourceParentType</span></span>
<span data-ttu-id="48e2f-124">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="48e2f-124">The parent resource type.</span></span>

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

### <span data-ttu-id="48e2f-125">-</span><span class="sxs-lookup"><span data-stu-id="48e2f-125">-ResourceType</span></span>
<span data-ttu-id="48e2f-126">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="48e2f-126">The resource type.</span></span>

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

### <span data-ttu-id="48e2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e2f-127">CommonParameters</span></span>
<span data-ttu-id="48e2f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48e2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e2f-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48e2f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e2f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48e2f-130">INPUTS</span></span>

### <span data-ttu-id="48e2f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="48e2f-131">System.String</span></span>

## <span data-ttu-id="48e2f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48e2f-132">OUTPUTS</span></span>

### <span data-ttu-id="48e2f-133">Microsoft. Azure. Commands. Maintenance. Models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="48e2f-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="48e2f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="48e2f-134">NOTES</span></span>

## <span data-ttu-id="48e2f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48e2f-135">RELATED LINKS</span></span>
