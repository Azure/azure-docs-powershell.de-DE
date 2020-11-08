---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176934"
---
# <span data-ttu-id="a9a31-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="a9a31-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="a9a31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9a31-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a31-103">Löscht eine Sicherheits Beurteilungs Metadaten aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9a31-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="a9a31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9a31-104">SYNTAX</span></span>

### <span data-ttu-id="a9a31-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9a31-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9a31-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9a31-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9a31-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a9a31-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9a31-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9a31-108">DESCRIPTION</span></span>
<span data-ttu-id="a9a31-109">Löscht eine Sicherheits Beurteilungs Metadaten aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9a31-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="a9a31-110">Mit dieser Aktion werden der Bewertungstyp und alle relevanten Bewertungsergebnisse aus dem Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a9a31-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="a9a31-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9a31-111">EXAMPLES</span></span>

### <span data-ttu-id="a9a31-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9a31-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="a9a31-113">Löschen eines Bewertungstyps aus einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="a9a31-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="a9a31-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9a31-114">PARAMETERS</span></span>

### <span data-ttu-id="a9a31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a31-115">-DefaultProfile</span></span>
<span data-ttu-id="a9a31-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9a31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9a31-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9a31-117">-InputObject</span></span>
<span data-ttu-id="a9a31-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="a9a31-118">Input Object.</span></span>

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

### <span data-ttu-id="a9a31-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a9a31-119">-Name</span></span>
<span data-ttu-id="a9a31-120">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="a9a31-120">Resource name.</span></span>

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

### <span data-ttu-id="a9a31-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9a31-121">-PassThru</span></span>
<span data-ttu-id="a9a31-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a9a31-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a9a31-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a9a31-123">-ResourceId</span></span>
<span data-ttu-id="a9a31-124">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="a9a31-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a9a31-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9a31-125">-Confirm</span></span>
<span data-ttu-id="a9a31-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9a31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9a31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a31-127">-WhatIf</span></span>
<span data-ttu-id="a9a31-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9a31-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9a31-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9a31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9a31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a31-130">CommonParameters</span></span>
<span data-ttu-id="a9a31-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9a31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a31-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9a31-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a31-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9a31-133">INPUTS</span></span>

### <span data-ttu-id="a9a31-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a9a31-134">System.String</span></span>

### <span data-ttu-id="a9a31-135">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="a9a31-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="a9a31-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9a31-136">OUTPUTS</span></span>

### <span data-ttu-id="a9a31-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9a31-137">System.Boolean</span></span>

## <span data-ttu-id="a9a31-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9a31-138">NOTES</span></span>

## <span data-ttu-id="a9a31-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9a31-139">RELATED LINKS</span></span>
