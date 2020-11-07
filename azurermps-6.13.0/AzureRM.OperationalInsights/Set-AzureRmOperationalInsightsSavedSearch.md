---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3af374d6609a7063581e06aa8aa496e56a1fd45c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662795"
---
# <span data-ttu-id="639a7-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="639a7-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="639a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="639a7-102">SYNOPSIS</span></span>
<span data-ttu-id="639a7-103">Aktualisiert eine gespeicherte Suche, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="639a7-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="639a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="639a7-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="639a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="639a7-105">DESCRIPTION</span></span>
<span data-ttu-id="639a7-106">Das Cmdlet " **Satz-AzureRmOperationalInsightsSavedSearch** " aktualisiert eine gespeicherte Suche, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="639a7-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="639a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="639a7-107">EXAMPLES</span></span>

### <span data-ttu-id="639a7-108">Beispiel 1: legt eine gespeicherte Suche mit aktualisierten Eigenschaften fest</span><span class="sxs-lookup"><span data-stu-id="639a7-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="639a7-109">Mit diesem Befehl wird eine gespeicherte Suche mit aktualisierten Eigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="639a7-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="639a7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="639a7-110">PARAMETERS</span></span>

### <span data-ttu-id="639a7-111">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="639a7-111">-Category</span></span>
<span data-ttu-id="639a7-112">Gibt den Namen der Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="639a7-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="639a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="639a7-113">-DefaultProfile</span></span>
<span data-ttu-id="639a7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="639a7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="639a7-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="639a7-115">-DisplayName</span></span>
<span data-ttu-id="639a7-116">Gibt den Anzeigenamen an.</span><span class="sxs-lookup"><span data-stu-id="639a7-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="639a7-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="639a7-117">-ETag</span></span>
<span data-ttu-id="639a7-118">Gibt den ETag-Namen an.</span><span class="sxs-lookup"><span data-stu-id="639a7-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="639a7-119">-Query</span><span class="sxs-lookup"><span data-stu-id="639a7-119">-Query</span></span>
<span data-ttu-id="639a7-120">Gibt den Abfragenamen an.</span><span class="sxs-lookup"><span data-stu-id="639a7-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="639a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="639a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="639a7-122">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="639a7-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="639a7-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="639a7-123">-SavedSearchId</span></span>
<span data-ttu-id="639a7-124">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="639a7-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="639a7-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="639a7-125">-Tag</span></span>
<span data-ttu-id="639a7-126">Die gespeicherten Suchkategorien.</span><span class="sxs-lookup"><span data-stu-id="639a7-126">The saved search tags.</span></span>

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

### <span data-ttu-id="639a7-127">-Version</span><span class="sxs-lookup"><span data-stu-id="639a7-127">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="639a7-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="639a7-128">-WorkspaceName</span></span>
<span data-ttu-id="639a7-129">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="639a7-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="639a7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="639a7-130">CommonParameters</span></span>
<span data-ttu-id="639a7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="639a7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="639a7-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="639a7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="639a7-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="639a7-133">INPUTS</span></span>

### <span data-ttu-id="639a7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="639a7-134">System.String</span></span>

### <span data-ttu-id="639a7-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="639a7-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="639a7-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="639a7-136">System.Int64</span></span>

## <span data-ttu-id="639a7-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="639a7-137">OUTPUTS</span></span>

### <span data-ttu-id="639a7-138">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="639a7-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="639a7-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="639a7-139">NOTES</span></span>

## <span data-ttu-id="639a7-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="639a7-140">RELATED LINKS</span></span>

[<span data-ttu-id="639a7-141">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="639a7-141">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


