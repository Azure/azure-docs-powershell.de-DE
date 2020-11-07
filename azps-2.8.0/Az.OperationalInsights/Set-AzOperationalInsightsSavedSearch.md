---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 535fbe737184b996ee0caa030c83137ea8cd1019
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847936"
---
# <span data-ttu-id="2ac19-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="2ac19-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="2ac19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ac19-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac19-103">Aktualisiert eine gespeicherte Suche, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2ac19-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="2ac19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ac19-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ac19-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ac19-105">DESCRIPTION</span></span>
<span data-ttu-id="2ac19-106">Das Cmdlet " **Satz-AzOperationalInsightsSavedSearch** " aktualisiert eine gespeicherte Suche, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2ac19-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="2ac19-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ac19-107">EXAMPLES</span></span>

### <span data-ttu-id="2ac19-108">Beispiel 1: legt eine gespeicherte Suche mit aktualisierten Eigenschaften fest</span><span class="sxs-lookup"><span data-stu-id="2ac19-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="2ac19-109">Mit diesem Befehl wird eine gespeicherte Suche mit aktualisierten Eigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2ac19-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="2ac19-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ac19-110">PARAMETERS</span></span>

### <span data-ttu-id="2ac19-111">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="2ac19-111">-Category</span></span>
<span data-ttu-id="2ac19-112">Gibt den Namen der Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="2ac19-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac19-113">-DefaultProfile</span></span>
<span data-ttu-id="2ac19-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2ac19-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ac19-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2ac19-115">-DisplayName</span></span>
<span data-ttu-id="2ac19-116">Gibt den Anzeigenamen an.</span><span class="sxs-lookup"><span data-stu-id="2ac19-116">Specifies the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac19-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="2ac19-117">-ETag</span></span>
<span data-ttu-id="2ac19-118">Gibt den ETag-Namen an.</span><span class="sxs-lookup"><span data-stu-id="2ac19-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac19-119">-Query</span><span class="sxs-lookup"><span data-stu-id="2ac19-119">-Query</span></span>
<span data-ttu-id="2ac19-120">Gibt den Abfragenamen an.</span><span class="sxs-lookup"><span data-stu-id="2ac19-120">Specifies the query name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac19-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac19-121">-ResourceGroupName</span></span>
<span data-ttu-id="2ac19-122">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2ac19-122">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac19-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="2ac19-123">-SavedSearchId</span></span>
<span data-ttu-id="2ac19-124">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="2ac19-124">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac19-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ac19-125">-Tag</span></span>
<span data-ttu-id="2ac19-126">Die gespeicherten Suchkategorien.</span><span class="sxs-lookup"><span data-stu-id="2ac19-126">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac19-127">-Version</span><span class="sxs-lookup"><span data-stu-id="2ac19-127">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac19-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2ac19-128">-WorkspaceName</span></span>
<span data-ttu-id="2ac19-129">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="2ac19-129">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac19-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac19-130">CommonParameters</span></span>
<span data-ttu-id="2ac19-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac19-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac19-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac19-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac19-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ac19-133">INPUTS</span></span>

### <span data-ttu-id="2ac19-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac19-134">System.String</span></span>

### <span data-ttu-id="2ac19-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ac19-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2ac19-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="2ac19-136">System.Int64</span></span>

## <span data-ttu-id="2ac19-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ac19-137">OUTPUTS</span></span>

### <span data-ttu-id="2ac19-138">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="2ac19-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="2ac19-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ac19-139">NOTES</span></span>

## <span data-ttu-id="2ac19-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ac19-140">RELATED LINKS</span></span>

[<span data-ttu-id="2ac19-141">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="2ac19-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


