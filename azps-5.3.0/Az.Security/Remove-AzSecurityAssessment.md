---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377725"
---
# <span data-ttu-id="6dd59-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="6dd59-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="6dd59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dd59-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd59-103">Löscht ein Sicherheitsbewertungsergebnis aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6dd59-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="6dd59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6dd59-104">SYNTAX</span></span>

### <span data-ttu-id="6dd59-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="6dd59-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd59-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="6dd59-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd59-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dd59-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd59-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="6dd59-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dd59-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6dd59-109">DESCRIPTION</span></span>
<span data-ttu-id="6dd59-110">Löscht ein Sicherheitsbewertungsergebnis aus einem Abonnement, das in der Regel verwendet wird, wenn eine Neuauswertung gelöscht wird oder die Bewertung für eine bestimmte Ressource nicht mehr relevant ist.</span><span class="sxs-lookup"><span data-stu-id="6dd59-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="6dd59-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6dd59-111">EXAMPLES</span></span>

### <span data-ttu-id="6dd59-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6dd59-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="6dd59-113">Löscht ein Bewertungsergebnis für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="6dd59-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="6dd59-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dd59-114">PARAMETERS</span></span>

### <span data-ttu-id="6dd59-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="6dd59-115">-AssessedResourceId</span></span>
<span data-ttu-id="6dd59-116">Vollständige Ressourcen-ID der Ressource, für die die Bewertung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="6dd59-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd59-117">-DefaultProfile</span></span>
<span data-ttu-id="6dd59-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6dd59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd59-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dd59-119">-InputObject</span></span>
<span data-ttu-id="6dd59-120">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="6dd59-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd59-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6dd59-121">-Name</span></span>
<span data-ttu-id="6dd59-122">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="6dd59-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd59-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dd59-123">-PassThru</span></span>
<span data-ttu-id="6dd59-124">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="6dd59-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="6dd59-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dd59-125">-ResourceId</span></span>
<span data-ttu-id="6dd59-126">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="6dd59-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd59-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dd59-127">-Confirm</span></span>
<span data-ttu-id="6dd59-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6dd59-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dd59-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6dd59-129">-WhatIf</span></span>
<span data-ttu-id="6dd59-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6dd59-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dd59-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6dd59-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dd59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd59-132">CommonParameters</span></span>
<span data-ttu-id="6dd59-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd59-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dd59-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd59-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6dd59-135">INPUTS</span></span>

### <span data-ttu-id="6dd59-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6dd59-136">System.String</span></span>

### <span data-ttu-id="6dd59-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="6dd59-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="6dd59-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6dd59-138">OUTPUTS</span></span>

### <span data-ttu-id="6dd59-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6dd59-139">System.Boolean</span></span>

## <span data-ttu-id="6dd59-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6dd59-140">NOTES</span></span>

## <span data-ttu-id="6dd59-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6dd59-141">RELATED LINKS</span></span>
