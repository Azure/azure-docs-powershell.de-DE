---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146057"
---
# <span data-ttu-id="09c90-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="09c90-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="09c90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09c90-102">SYNOPSIS</span></span>
<span data-ttu-id="09c90-103">Ruft verwaltete Anwendungen ab</span><span class="sxs-lookup"><span data-stu-id="09c90-103">Gets managed applications</span></span>

## <span data-ttu-id="09c90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09c90-104">SYNTAX</span></span>

### <span data-ttu-id="09c90-105">GetBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="09c90-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09c90-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="09c90-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09c90-107">GetById</span><span class="sxs-lookup"><span data-stu-id="09c90-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09c90-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09c90-108">DESCRIPTION</span></span>
<span data-ttu-id="09c90-109">Das **Cmdlet "Get-AzManagedApplication"** ruft verwaltete Anwendungen ab</span><span class="sxs-lookup"><span data-stu-id="09c90-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="09c90-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09c90-110">EXAMPLES</span></span>

### <span data-ttu-id="09c90-111">Beispiel 1: Alle verwalteten Anwendungen unter einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="09c90-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="09c90-112">Dieser Befehl ruft verwaltete Anwendungen unter der Ressourcengruppe "MyRG" ab.</span><span class="sxs-lookup"><span data-stu-id="09c90-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="09c90-113">Beispiel 2: Alle verwalteten Anwendungen erhalten</span><span class="sxs-lookup"><span data-stu-id="09c90-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="09c90-114">Mit diesem Befehl werden alle verwalteten Anwendungen unter dem aktuellen Abonnement angezeigt</span><span class="sxs-lookup"><span data-stu-id="09c90-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="09c90-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09c90-115">PARAMETERS</span></span>

### <span data-ttu-id="09c90-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="09c90-116">-ApiVersion</span></span>
<span data-ttu-id="09c90-117">Gibt im festgelegten Satz die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="09c90-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="09c90-118">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="09c90-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c90-119">-DefaultProfile</span></span>
<span data-ttu-id="09c90-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09c90-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09c90-121">-ID</span><span class="sxs-lookup"><span data-stu-id="09c90-121">-Id</span></span>
<span data-ttu-id="09c90-122">Die vollqualifizierte verwaltete Anwendungs-ID einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="09c90-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="09c90-123">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="09c90-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c90-124">-Name</span><span class="sxs-lookup"><span data-stu-id="09c90-124">-Name</span></span>
<span data-ttu-id="09c90-125">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="09c90-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c90-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="09c90-126">-Pre</span></span>
<span data-ttu-id="09c90-127">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09c90-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="09c90-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09c90-128">-ResourceGroupName</span></span>
<span data-ttu-id="09c90-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="09c90-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c90-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c90-130">CommonParameters</span></span>
<span data-ttu-id="09c90-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c90-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c90-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09c90-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c90-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09c90-133">INPUTS</span></span>

### <span data-ttu-id="09c90-134">System.String</span><span class="sxs-lookup"><span data-stu-id="09c90-134">System.String</span></span>

## <span data-ttu-id="09c90-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09c90-135">OUTPUTS</span></span>

### <span data-ttu-id="09c90-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="09c90-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="09c90-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="09c90-137">NOTES</span></span>

## <span data-ttu-id="09c90-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="09c90-138">RELATED LINKS</span></span>
