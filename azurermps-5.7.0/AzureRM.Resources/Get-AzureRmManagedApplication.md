---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 3dd86c186d05ce59f237be51b8e059e800c47a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663440"
---
# <span data-ttu-id="93327-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="93327-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="93327-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93327-102">SYNOPSIS</span></span>
<span data-ttu-id="93327-103">Ruft verwaltete Anwendungen ab</span><span class="sxs-lookup"><span data-stu-id="93327-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93327-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93327-104">SYNTAX</span></span>

### <span data-ttu-id="93327-105">GetBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="93327-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93327-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93327-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93327-107">GetById</span><span class="sxs-lookup"><span data-stu-id="93327-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93327-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93327-108">DESCRIPTION</span></span>
<span data-ttu-id="93327-109">Das Cmdlet " **Get-AzureRmManagedApplication** " ruft verwaltete Anwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="93327-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="93327-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93327-110">EXAMPLES</span></span>

### <span data-ttu-id="93327-111">Beispiel 1: Abrufen aller verwalteten Anwendungen unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="93327-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="93327-112">Dieser Befehl ruft verwaltete Anwendungen unter Ressourcengruppe "MyRG" ab.</span><span class="sxs-lookup"><span data-stu-id="93327-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="93327-113">Beispiel 2: Abrufen aller verwalteten Anwendungen</span><span class="sxs-lookup"><span data-stu-id="93327-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="93327-114">Mit diesem Befehl werden alle verwalteten Anwendungen unter dem aktuellen Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="93327-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="93327-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="93327-115">PARAMETERS</span></span>

### <span data-ttu-id="93327-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="93327-116">-ApiVersion</span></span>
<span data-ttu-id="93327-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93327-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="93327-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="93327-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93327-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93327-119">-DefaultProfile</span></span>
<span data-ttu-id="93327-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93327-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93327-121">-ID</span><span class="sxs-lookup"><span data-stu-id="93327-121">-Id</span></span>
<span data-ttu-id="93327-122">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="93327-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="93327-123">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="93327-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-124">-Name</span><span class="sxs-lookup"><span data-stu-id="93327-124">-Name</span></span>
<span data-ttu-id="93327-125">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="93327-125">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="93327-126">-Pre</span></span>
<span data-ttu-id="93327-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="93327-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="93327-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93327-128">-ResourceGroupName</span></span>
<span data-ttu-id="93327-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="93327-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93327-130">CommonParameters</span></span>
<span data-ttu-id="93327-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93327-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93327-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93327-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93327-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93327-133">INPUTS</span></span>

### <span data-ttu-id="93327-134">System. String</span><span class="sxs-lookup"><span data-stu-id="93327-134">System.String</span></span>

## <span data-ttu-id="93327-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93327-135">OUTPUTS</span></span>

### <span data-ttu-id="93327-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="93327-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="93327-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="93327-137">NOTES</span></span>

## <span data-ttu-id="93327-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93327-138">RELATED LINKS</span></span>
