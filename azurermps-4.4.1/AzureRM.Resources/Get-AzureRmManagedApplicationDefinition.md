---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: ef724c4d2e9771243058471c3ce2aebc944d2bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662618"
---
# <span data-ttu-id="71441-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="71441-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="71441-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71441-102">SYNOPSIS</span></span>
<span data-ttu-id="71441-103">Ruft Definitionen für verwaltete Anwendungen ab</span><span class="sxs-lookup"><span data-stu-id="71441-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71441-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71441-104">SYNTAX</span></span>

### <span data-ttu-id="71441-105">Der Parametersatz für verwaltete Anwendungsdefinitionsnamen.</span><span class="sxs-lookup"><span data-stu-id="71441-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="71441-106">Standard</span><span class="sxs-lookup"><span data-stu-id="71441-106">(Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71441-107">Der Parametersatz der verwalteten Anwendungs Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="71441-107">The managed application definition Id parameter set.</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71441-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71441-108">DESCRIPTION</span></span>
<span data-ttu-id="71441-109">Das Cmdlet " **Get-AzureRmManagedApplicationDefinition** " ruft verwaltete Anwendungsdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="71441-109">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="71441-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71441-110">EXAMPLES</span></span>

### <span data-ttu-id="71441-111">Beispiel 1: Abrufen aller verwalteten Anwendungsdefinitionen unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="71441-111">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="71441-112">Dieser Befehl ruft die Definitionen verwalteter Anwendungen unter Ressourcengruppe "MyRG" ab.</span><span class="sxs-lookup"><span data-stu-id="71441-112">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="71441-113">Beispiel 2: Abrufen einer Definition einer verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="71441-113">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="71441-114">Dieser Befehl ruft die verwaltete Anwendungsdefinition "myManagedAppDef" unter Ressourcengruppe "MyRG" ab.</span><span class="sxs-lookup"><span data-stu-id="71441-114">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="71441-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="71441-115">PARAMETERS</span></span>

### <span data-ttu-id="71441-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="71441-116">-ApiVersion</span></span>
<span data-ttu-id="71441-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="71441-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="71441-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="71441-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="71441-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71441-119">-DefaultProfile</span></span>
<span data-ttu-id="71441-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71441-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71441-121">-ID</span><span class="sxs-lookup"><span data-stu-id="71441-121">-Id</span></span>
<span data-ttu-id="71441-122">Die vollqualifizierte Definitions-ID der verwalteten Anwendung einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="71441-122">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="71441-123">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="71441-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71441-124">-Name</span><span class="sxs-lookup"><span data-stu-id="71441-124">-Name</span></span>
<span data-ttu-id="71441-125">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="71441-125">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71441-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="71441-126">-Pre</span></span>
<span data-ttu-id="71441-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="71441-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="71441-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71441-128">-ResourceGroupName</span></span>
<span data-ttu-id="71441-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71441-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71441-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71441-130">CommonParameters</span></span>
<span data-ttu-id="71441-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71441-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71441-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71441-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71441-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71441-133">INPUTS</span></span>

### <span data-ttu-id="71441-134">System. String</span><span class="sxs-lookup"><span data-stu-id="71441-134">System.String</span></span>

## <span data-ttu-id="71441-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71441-135">OUTPUTS</span></span>

### <span data-ttu-id="71441-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="71441-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="71441-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="71441-137">NOTES</span></span>

## <span data-ttu-id="71441-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71441-138">RELATED LINKS</span></span>

