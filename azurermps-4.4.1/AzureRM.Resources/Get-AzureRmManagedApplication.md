---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 953a810585550ec8895fc9306f78633beb4846a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478966"
---
# <span data-ttu-id="f23af-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="f23af-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="f23af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f23af-102">SYNOPSIS</span></span>
<span data-ttu-id="f23af-103">Ruft verwaltete Anwendungen ab</span><span class="sxs-lookup"><span data-stu-id="f23af-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f23af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f23af-104">SYNTAX</span></span>

### <span data-ttu-id="f23af-105">Der Parametersatz "alle verwalteten Anwendungen auflisten".</span><span class="sxs-lookup"><span data-stu-id="f23af-105">The list all managed applications parameter set.</span></span> <span data-ttu-id="f23af-106">Standard</span><span class="sxs-lookup"><span data-stu-id="f23af-106">(Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f23af-107">Der Parametersatz für verwaltete Anwendungsnamen.</span><span class="sxs-lookup"><span data-stu-id="f23af-107">The managed application name parameter set.</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f23af-108">Der Parametersatz der verwalteten Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="f23af-108">The managed application Id parameter set.</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f23af-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f23af-109">DESCRIPTION</span></span>
<span data-ttu-id="f23af-110">Das Cmdlet " **Get-AzureRmManagedApplication** " ruft verwaltete Anwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="f23af-110">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="f23af-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f23af-111">EXAMPLES</span></span>

### <span data-ttu-id="f23af-112">Beispiel 1: Abrufen aller verwalteten Anwendungen unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f23af-112">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="f23af-113">Dieser Befehl ruft verwaltete Anwendungen unter Ressourcengruppe "MyRG" ab.</span><span class="sxs-lookup"><span data-stu-id="f23af-113">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="f23af-114">Beispiel 2: Abrufen aller verwalteten Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f23af-114">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="f23af-115">Mit diesem Befehl werden alle verwalteten Anwendungen unter dem aktuellen Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f23af-115">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="f23af-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f23af-116">PARAMETERS</span></span>

### <span data-ttu-id="f23af-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f23af-117">-ApiVersion</span></span>
<span data-ttu-id="f23af-118">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f23af-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f23af-119">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f23af-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f23af-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23af-120">-DefaultProfile</span></span>
<span data-ttu-id="f23af-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f23af-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f23af-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f23af-122">-Id</span></span>
<span data-ttu-id="f23af-123">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="f23af-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="f23af-124">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f23af-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23af-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f23af-125">-Name</span></span>
<span data-ttu-id="f23af-126">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f23af-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23af-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="f23af-127">-Pre</span></span>
<span data-ttu-id="f23af-128">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="f23af-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f23af-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f23af-129">-ResourceGroupName</span></span>
<span data-ttu-id="f23af-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f23af-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23af-131">CommonParameters</span></span>
<span data-ttu-id="f23af-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f23af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23af-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23af-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23af-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f23af-134">INPUTS</span></span>

### <span data-ttu-id="f23af-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f23af-135">System.String</span></span>

## <span data-ttu-id="f23af-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f23af-136">OUTPUTS</span></span>

### <span data-ttu-id="f23af-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f23af-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f23af-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f23af-138">NOTES</span></span>

## <span data-ttu-id="f23af-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f23af-139">RELATED LINKS</span></span>

