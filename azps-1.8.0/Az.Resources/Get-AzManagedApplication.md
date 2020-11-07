---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: 9c670973c9fcff3cd9038809cb955efc32edeee0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659650"
---
# <span data-ttu-id="6a760-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="6a760-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="6a760-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a760-102">SYNOPSIS</span></span>
<span data-ttu-id="6a760-103">Ruft verwaltete Anwendungen ab</span><span class="sxs-lookup"><span data-stu-id="6a760-103">Gets managed applications</span></span>

## <span data-ttu-id="6a760-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a760-104">SYNTAX</span></span>

### <span data-ttu-id="6a760-105">GetBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a760-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a760-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6a760-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a760-107">GetById</span><span class="sxs-lookup"><span data-stu-id="6a760-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a760-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a760-108">DESCRIPTION</span></span>
<span data-ttu-id="6a760-109">Das Cmdlet " **Get-AzManagedApplication** " ruft verwaltete Anwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="6a760-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="6a760-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a760-110">EXAMPLES</span></span>

### <span data-ttu-id="6a760-111">Beispiel 1: Abrufen aller verwalteten Anwendungen unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6a760-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="6a760-112">Dieser Befehl ruft verwaltete Anwendungen unter Ressourcengruppe "MyRG" ab.</span><span class="sxs-lookup"><span data-stu-id="6a760-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="6a760-113">Beispiel 2: Abrufen aller verwalteten Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6a760-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="6a760-114">Mit diesem Befehl werden alle verwalteten Anwendungen unter dem aktuellen Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6a760-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="6a760-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a760-115">PARAMETERS</span></span>

### <span data-ttu-id="6a760-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6a760-116">-ApiVersion</span></span>
<span data-ttu-id="6a760-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6a760-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6a760-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6a760-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6a760-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a760-119">-DefaultProfile</span></span>
<span data-ttu-id="6a760-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a760-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a760-121">-ID</span><span class="sxs-lookup"><span data-stu-id="6a760-121">-Id</span></span>
<span data-ttu-id="6a760-122">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="6a760-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="6a760-123">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="6a760-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="6a760-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6a760-124">-Name</span></span>
<span data-ttu-id="6a760-125">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6a760-125">The managed application name.</span></span>

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

### <span data-ttu-id="6a760-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="6a760-126">-Pre</span></span>
<span data-ttu-id="6a760-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="6a760-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6a760-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a760-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a760-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6a760-129">The resource group name.</span></span>

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

### <span data-ttu-id="6a760-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a760-130">CommonParameters</span></span>
<span data-ttu-id="6a760-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a760-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a760-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a760-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a760-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a760-133">INPUTS</span></span>

### <span data-ttu-id="6a760-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6a760-134">System.String</span></span>

## <span data-ttu-id="6a760-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a760-135">OUTPUTS</span></span>

### <span data-ttu-id="6a760-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6a760-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6a760-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a760-137">NOTES</span></span>

## <span data-ttu-id="6a760-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a760-138">RELATED LINKS</span></span>
