---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174212"
---
# <span data-ttu-id="4446f-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="4446f-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="4446f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4446f-102">SYNOPSIS</span></span>
<span data-ttu-id="4446f-103">Löscht die Metadaten einer Sicherheitsbewertung aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4446f-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="4446f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4446f-104">SYNTAX</span></span>

### <span data-ttu-id="4446f-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="4446f-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4446f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4446f-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4446f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4446f-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4446f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4446f-108">DESCRIPTION</span></span>
<span data-ttu-id="4446f-109">Löscht die Metadaten einer Sicherheitsbewertung aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4446f-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="4446f-110">Durch diese Aktion werden der Bewertungstyp und alle relevanten Bewertungsergebnisse aus dem Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4446f-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="4446f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4446f-111">EXAMPLES</span></span>

### <span data-ttu-id="4446f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4446f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="4446f-113">Löscht einen Bewertungstyp aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4446f-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="4446f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4446f-114">PARAMETERS</span></span>

### <span data-ttu-id="4446f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4446f-115">-DefaultProfile</span></span>
<span data-ttu-id="4446f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4446f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4446f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4446f-117">-InputObject</span></span>
<span data-ttu-id="4446f-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="4446f-118">Input Object.</span></span>

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

### <span data-ttu-id="4446f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4446f-119">-Name</span></span>
<span data-ttu-id="4446f-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="4446f-120">Resource name.</span></span>

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

### <span data-ttu-id="4446f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4446f-121">-PassThru</span></span>
<span data-ttu-id="4446f-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4446f-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="4446f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4446f-123">-ResourceId</span></span>
<span data-ttu-id="4446f-124">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="4446f-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="4446f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4446f-125">-Confirm</span></span>
<span data-ttu-id="4446f-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4446f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4446f-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4446f-127">-WhatIf</span></span>
<span data-ttu-id="4446f-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4446f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4446f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4446f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4446f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4446f-130">CommonParameters</span></span>
<span data-ttu-id="4446f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4446f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4446f-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4446f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4446f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4446f-133">INPUTS</span></span>

### <span data-ttu-id="4446f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4446f-134">System.String</span></span>

### <span data-ttu-id="4446f-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="4446f-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="4446f-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4446f-136">OUTPUTS</span></span>

### <span data-ttu-id="4446f-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4446f-137">System.Boolean</span></span>

## <span data-ttu-id="4446f-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4446f-138">NOTES</span></span>

## <span data-ttu-id="4446f-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4446f-139">RELATED LINKS</span></span>
