---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: daa0d87eab24743863e6cbbcdd1c010e974c113c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929784"
---
# <span data-ttu-id="542f1-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="542f1-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="542f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="542f1-102">SYNOPSIS</span></span>
<span data-ttu-id="542f1-103">Löscht eine Sicherheitsbewertungsmetadaten aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="542f1-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="542f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="542f1-104">SYNTAX</span></span>

### <span data-ttu-id="542f1-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="542f1-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="542f1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="542f1-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="542f1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="542f1-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="542f1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="542f1-108">DESCRIPTION</span></span>
<span data-ttu-id="542f1-109">Löscht eine Sicherheitsbewertungsmetadaten aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="542f1-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="542f1-110">Mit dieser Aktion werden der Bewertungstyp und alle relevanten Bewertungsergebnisse aus dem Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="542f1-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="542f1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="542f1-111">EXAMPLES</span></span>

### <span data-ttu-id="542f1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="542f1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="542f1-113">Löscht einen Bewertungstyp aus einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="542f1-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="542f1-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="542f1-114">PARAMETERS</span></span>

### <span data-ttu-id="542f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542f1-115">-DefaultProfile</span></span>
<span data-ttu-id="542f1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="542f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="542f1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="542f1-117">-InputObject</span></span>
<span data-ttu-id="542f1-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="542f1-118">Input Object.</span></span>

```yaml
Type: PSSecurityAssessmentMetadata
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="542f1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="542f1-119">-Name</span></span>
<span data-ttu-id="542f1-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="542f1-120">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="542f1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="542f1-121">-PassThru</span></span>
<span data-ttu-id="542f1-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="542f1-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="542f1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="542f1-123">-ResourceId</span></span>
<span data-ttu-id="542f1-124">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="542f1-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="542f1-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="542f1-125">-Confirm</span></span>
<span data-ttu-id="542f1-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="542f1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="542f1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="542f1-127">-WhatIf</span></span>
<span data-ttu-id="542f1-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="542f1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="542f1-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="542f1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="542f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542f1-130">CommonParameters</span></span>
<span data-ttu-id="542f1-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="542f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542f1-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="542f1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542f1-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="542f1-133">INPUTS</span></span>

### <span data-ttu-id="542f1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="542f1-134">System.String</span></span>

### <span data-ttu-id="542f1-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="542f1-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="542f1-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="542f1-136">OUTPUTS</span></span>

### <span data-ttu-id="542f1-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="542f1-137">System.Boolean</span></span>

## <span data-ttu-id="542f1-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="542f1-138">NOTES</span></span>

## <span data-ttu-id="542f1-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="542f1-139">RELATED LINKS</span></span>
