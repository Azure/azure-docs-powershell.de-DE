---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 3853cc1785ca0e9f087b1e30870d17d304666df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652342"
---
# <span data-ttu-id="a29f0-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="a29f0-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="a29f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a29f0-102">SYNOPSIS</span></span>
<span data-ttu-id="a29f0-103">Importieren Sie eine Blueprint-Datei im JSON-Format in ein Blueprint-Objekt, und speichern Sie Sie in der angegebenen Abonnement-oder Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a29f0-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="a29f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a29f0-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a29f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a29f0-105">DESCRIPTION</span></span>
<span data-ttu-id="a29f0-106">Importieren Sie eine Blueprint-Definition mit ihren Artefakten.</span><span class="sxs-lookup"><span data-stu-id="a29f0-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="a29f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a29f0-107">EXAMPLES</span></span>

### <span data-ttu-id="a29f0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a29f0-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="a29f0-109">Importieren Sie eine Blueprint-Definition mit ihren Artefakten, und speichern Sie Sie in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a29f0-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="a29f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a29f0-110">PARAMETERS</span></span>

### <span data-ttu-id="a29f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29f0-111">-DefaultProfile</span></span>
<span data-ttu-id="a29f0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a29f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a29f0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a29f0-113">-Force</span></span>
<span data-ttu-id="a29f0-114">Wenn die Ausführung auf "true" festgelegt ist, werden Sie nicht aufgefordert, eine Bestätigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a29f0-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="a29f0-115">-InputPath</span><span class="sxs-lookup"><span data-stu-id="a29f0-115">-InputPath</span></span>
<span data-ttu-id="a29f0-116">Pfad zu einer Blueprint-JSON-Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a29f0-116">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29f0-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a29f0-117">-ManagementGroupId</span></span>
<span data-ttu-id="a29f0-118">Verwaltungsgruppen-ID, in der die Blueprint-Definition steht oder gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a29f0-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29f0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a29f0-119">-Name</span></span>
<span data-ttu-id="a29f0-120">Blueprint-Definitionsname</span><span class="sxs-lookup"><span data-stu-id="a29f0-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29f0-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a29f0-121">-SubscriptionId</span></span>
<span data-ttu-id="a29f0-122">Die Abonnement-ID, in der die Blueprint-Definition fest steht oder gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a29f0-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29f0-123">CommonParameters</span></span>
<span data-ttu-id="a29f0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a29f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a29f0-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a29f0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29f0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a29f0-126">INPUTS</span></span>

### <span data-ttu-id="a29f0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a29f0-127">System.String</span></span>

## <span data-ttu-id="a29f0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a29f0-128">OUTPUTS</span></span>

### <span data-ttu-id="a29f0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a29f0-129">System.String</span></span>

## <span data-ttu-id="a29f0-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a29f0-130">NOTES</span></span>

## <span data-ttu-id="a29f0-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a29f0-131">RELATED LINKS</span></span>
