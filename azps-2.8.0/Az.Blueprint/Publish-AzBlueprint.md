---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 5286b8953a9f28c5e63fe176f19d9d885e9c1d06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652336"
---
# <span data-ttu-id="3f8e3-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="3f8e3-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="3f8e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f8e3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f8e3-103">Veröffentlichen einer neuen Version eines Blueprints</span><span class="sxs-lookup"><span data-stu-id="3f8e3-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="3f8e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f8e3-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f8e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f8e3-105">DESCRIPTION</span></span>
<span data-ttu-id="3f8e3-106">Veröffentlichen einer neuen Version einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="3f8e3-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="3f8e3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f8e3-107">EXAMPLES</span></span>

### <span data-ttu-id="3f8e3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f8e3-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```
<span data-ttu-id="3f8e3-109">Veröffentlichen einer neuen Version einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="3f8e3-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="3f8e3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f8e3-110">PARAMETERS</span></span>

### <span data-ttu-id="3f8e3-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="3f8e3-111">-Blueprint</span></span>
<span data-ttu-id="3f8e3-112">Blueprint-Objekt</span><span class="sxs-lookup"><span data-stu-id="3f8e3-112">Blueprint object.</span></span>

```yaml
Type: PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f8e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f8e3-113">-DefaultProfile</span></span>
<span data-ttu-id="3f8e3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f8e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f8e3-115">-Version</span><span class="sxs-lookup"><span data-stu-id="3f8e3-115">-Version</span></span>
<span data-ttu-id="3f8e3-116">Version für die Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="3f8e3-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="3f8e3-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="3f8e3-117">-ChangeNote</span></span>
<span data-ttu-id="3f8e3-118">Hinweise zum Beschreiben des Inhalts dieser Blueprint-Version.</span><span class="sxs-lookup"><span data-stu-id="3f8e3-118">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="3f8e3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f8e3-119">CommonParameters</span></span>
<span data-ttu-id="3f8e3-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f8e3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3f8e3-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f8e3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f8e3-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f8e3-122">INPUTS</span></span>

### <span data-ttu-id="3f8e3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3f8e3-123">System.String</span></span>

### <span data-ttu-id="3f8e3-124">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="3f8e3-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="3f8e3-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f8e3-125">OUTPUTS</span></span>

### <span data-ttu-id="3f8e3-126">Microsoft. Azure. Commands. Blueprint. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="3f8e3-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="3f8e3-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f8e3-127">NOTES</span></span>

## <span data-ttu-id="3f8e3-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f8e3-128">RELATED LINKS</span></span>
