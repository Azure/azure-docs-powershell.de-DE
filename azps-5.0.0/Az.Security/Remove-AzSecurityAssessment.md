---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176935"
---
# <span data-ttu-id="ad8ce-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="ad8ce-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="ad8ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad8ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ad8ce-103">Löscht ein Ergebnis der Sicherheitsbewertung aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad8ce-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="ad8ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad8ce-104">SYNTAX</span></span>

### <span data-ttu-id="ad8ce-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad8ce-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad8ce-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="ad8ce-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad8ce-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad8ce-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad8ce-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="ad8ce-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad8ce-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad8ce-109">DESCRIPTION</span></span>
<span data-ttu-id="ad8ce-110">Löscht ein Ergebnis einer Sicherheitsbewertung aus einem Abonnement, das in der Regel verwendet wird, wenn ein resoruce gelöscht wird oder wenn die Bewertung für eine bestimmte Ressource nicht mehr relevant ist</span><span class="sxs-lookup"><span data-stu-id="ad8ce-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="ad8ce-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad8ce-111">EXAMPLES</span></span>

### <span data-ttu-id="ad8ce-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad8ce-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="ad8ce-113">Löschen eines Bewertungsergebnisses für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="ad8ce-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="ad8ce-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad8ce-114">PARAMETERS</span></span>

### <span data-ttu-id="ad8ce-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="ad8ce-115">-AssessedResourceId</span></span>
<span data-ttu-id="ad8ce-116">Die vollständige Ressourcen-ID der Ressource, auf der die Bewertung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="ad8ce-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="ad8ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad8ce-117">-DefaultProfile</span></span>
<span data-ttu-id="ad8ce-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad8ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad8ce-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ad8ce-119">-InputObject</span></span>
<span data-ttu-id="ad8ce-120">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="ad8ce-120">Input Object.</span></span>

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

### <span data-ttu-id="ad8ce-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ad8ce-121">-Name</span></span>
<span data-ttu-id="ad8ce-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="ad8ce-122">Resource name.</span></span>

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

### <span data-ttu-id="ad8ce-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad8ce-123">-PassThru</span></span>
<span data-ttu-id="ad8ce-124">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ad8ce-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="ad8ce-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ad8ce-125">-ResourceId</span></span>
<span data-ttu-id="ad8ce-126">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="ad8ce-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ad8ce-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad8ce-127">-Confirm</span></span>
<span data-ttu-id="ad8ce-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad8ce-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad8ce-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad8ce-129">-WhatIf</span></span>
<span data-ttu-id="ad8ce-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad8ce-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad8ce-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad8ce-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad8ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad8ce-132">CommonParameters</span></span>
<span data-ttu-id="ad8ce-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad8ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad8ce-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad8ce-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad8ce-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad8ce-135">INPUTS</span></span>

### <span data-ttu-id="ad8ce-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ad8ce-136">System.String</span></span>

### <span data-ttu-id="ad8ce-137">Microsoft. Azure. Commands. Security. Models. Assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="ad8ce-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="ad8ce-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad8ce-138">OUTPUTS</span></span>

### <span data-ttu-id="ad8ce-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad8ce-139">System.Boolean</span></span>

## <span data-ttu-id="ad8ce-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad8ce-140">NOTES</span></span>

## <span data-ttu-id="ad8ce-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad8ce-141">RELATED LINKS</span></span>
