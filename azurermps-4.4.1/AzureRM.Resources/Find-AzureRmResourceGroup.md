---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481622"
---
# <span data-ttu-id="a5ad5-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5ad5-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="a5ad5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ad5-103">Sucht nach Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5ad5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5ad5-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5ad5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5ad5-105">DESCRIPTION</span></span>
<span data-ttu-id="a5ad5-106">Das Cmdlet " **Suchen-AzureRmResourceGroup** " sucht nach Ressourcengruppen, wobei die angegebenen Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="a5ad5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5ad5-107">EXAMPLES</span></span>

### <span data-ttu-id="a5ad5-108">Beispiel 1: Suchen nach allen Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="a5ad5-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="a5ad5-109">Dieser Befehl findet alle Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="a5ad5-110">Beispiel 2: Suchen nach Ressourcengruppen nach Tag-Name</span><span class="sxs-lookup"><span data-stu-id="a5ad5-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="a5ad5-111">Dieser Befehl findet alle Ressourcengruppen, die eine Kategorie mit dem Namen "Testtag" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="a5ad5-112">Beispiel 3: Suchen von Ressourcengruppen nach Tag-Name und-Wert</span><span class="sxs-lookup"><span data-stu-id="a5ad5-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="a5ad5-113">Dieser Befehl findet alle Ressourcengruppen mit dem Tag Testtag und dem Wert testVal.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="a5ad5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5ad5-114">PARAMETERS</span></span>

### <span data-ttu-id="a5ad5-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a5ad5-115">-ApiVersion</span></span>
<span data-ttu-id="a5ad5-116">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="a5ad5-117">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ad5-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="a5ad5-118">-Pre</span></span>
<span data-ttu-id="a5ad5-119">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ad5-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5ad5-120">-Tag</span></span>
<span data-ttu-id="a5ad5-121">Gibt Tag-Informationen als Hashtabelle an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-121">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="a5ad5-122">Verwenden Sie die folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="a5ad5-122">Use the following formats:</span></span>

<span data-ttu-id="a5ad5-123">@ {Tagname = $NULL} oder @ {Tagname = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-123">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5ad5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ad5-124">-DefaultProfile</span></span>
<span data-ttu-id="a5ad5-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5ad5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ad5-126">CommonParameters</span></span>
<span data-ttu-id="a5ad5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5ad5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ad5-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5ad5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ad5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5ad5-129">INPUTS</span></span>

## <span data-ttu-id="a5ad5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5ad5-130">OUTPUTS</span></span>

### <span data-ttu-id="a5ad5-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a5ad5-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a5ad5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5ad5-132">NOTES</span></span>

## <span data-ttu-id="a5ad5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5ad5-133">RELATED LINKS</span></span>

