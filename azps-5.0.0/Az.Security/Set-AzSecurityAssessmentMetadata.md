---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178208"
---
# <span data-ttu-id="9530a-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="9530a-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="9530a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9530a-102">SYNOPSIS</span></span>
<span data-ttu-id="9530a-103">Erstellt oder aktualisiert einen Typ für die Sicherheitsbewertung.</span><span class="sxs-lookup"><span data-stu-id="9530a-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="9530a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9530a-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9530a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9530a-105">DESCRIPTION</span></span>
<span data-ttu-id="9530a-106">Erstellt oder aktualisiert eine Sicherheits Bewertungs Metadaten, die zum Erstellen und Verwalten verschiedener Beurteilungs Eigenschaften verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9530a-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="9530a-107">Nach dieser Aktion werden Sie in der Lage sein, Bewertungsergebnisse für jede Ressource in diesem Abonnement zu melden.</span><span class="sxs-lookup"><span data-stu-id="9530a-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="9530a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9530a-108">EXAMPLES</span></span>

### <span data-ttu-id="9530a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9530a-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="9530a-110">Erstellen eines neuen Bewertungstyps in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="9530a-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="9530a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9530a-111">PARAMETERS</span></span>

### <span data-ttu-id="9530a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9530a-112">-DefaultProfile</span></span>
<span data-ttu-id="9530a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9530a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9530a-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9530a-114">-Description</span></span>
<span data-ttu-id="9530a-115">Detaillierte Zeichenfolge, die den Benutzern hilft, die Bedeutung dieser Bewertung und deren Berechnung zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="9530a-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="9530a-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9530a-116">-DisplayName</span></span>
<span data-ttu-id="9530a-117">Lesbarer Titel für dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="9530a-117">Human readable title for this object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9530a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9530a-118">-Name</span></span>
<span data-ttu-id="9530a-119">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="9530a-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9530a-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="9530a-120">-RemediationDescription</span></span>
<span data-ttu-id="9530a-121">Detaillierte Zeichenfolge, mit der die Benutzer die unterschiedlichen Methoden zum verringern oder beheben des Sicherheitsproblems verstehen können.</span><span class="sxs-lookup"><span data-stu-id="9530a-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="9530a-122">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="9530a-122">-Severity</span></span>
<span data-ttu-id="9530a-123">Zeigt die Wichtigkeit des Sicherheitsrisikos an, wenn die Bewertung fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="9530a-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="9530a-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9530a-124">-Confirm</span></span>
<span data-ttu-id="9530a-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9530a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9530a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9530a-126">-WhatIf</span></span>
<span data-ttu-id="9530a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9530a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9530a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9530a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9530a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9530a-129">CommonParameters</span></span>
<span data-ttu-id="9530a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9530a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9530a-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9530a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9530a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9530a-132">INPUTS</span></span>

### <span data-ttu-id="9530a-133">Keine</span><span class="sxs-lookup"><span data-stu-id="9530a-133">None</span></span>

## <span data-ttu-id="9530a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9530a-134">OUTPUTS</span></span>

### <span data-ttu-id="9530a-135">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="9530a-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="9530a-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="9530a-136">NOTES</span></span>

## <span data-ttu-id="9530a-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9530a-137">RELATED LINKS</span></span>
