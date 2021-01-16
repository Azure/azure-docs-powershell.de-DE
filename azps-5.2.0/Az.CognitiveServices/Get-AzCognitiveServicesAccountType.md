---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297022"
---
# <span data-ttu-id="ce797-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="ce797-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="ce797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce797-102">SYNOPSIS</span></span>
<span data-ttu-id="ce797-103">Ruft die verfügbaren Cognitive Services-Kontotypen ab.</span><span class="sxs-lookup"><span data-stu-id="ce797-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="ce797-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce797-104">SYNTAX</span></span>

### <span data-ttu-id="ce797-105">GetAccountTypes (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce797-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce797-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="ce797-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce797-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce797-107">DESCRIPTION</span></span>
<span data-ttu-id="ce797-108">Das **Cmdlet Get-AzCognitiveServicesAccountType** ruft die verfügbaren Cognitive Services-Kontotypen unter diesem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ce797-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="ce797-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce797-109">EXAMPLES</span></span>

### <span data-ttu-id="ce797-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce797-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="ce797-111">Hier finden Sie eine Liste der verfügbaren Typen.</span><span class="sxs-lookup"><span data-stu-id="ce797-111">Get the list of available Types.</span></span>

### <span data-ttu-id="ce797-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ce797-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="ce797-113">Hier finden Sie eine Liste der verfügbaren Typen in WestUs.</span><span class="sxs-lookup"><span data-stu-id="ce797-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="ce797-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ce797-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="ce797-115">Überprüfen Sie, ob es sich um einen gültigen Typnamen handelt, wird der Name zurückgegeben, `Face` wenn es sich um einen gültigen Namen handelt.</span><span class="sxs-lookup"><span data-stu-id="ce797-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="ce797-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce797-116">PARAMETERS</span></span>

### <span data-ttu-id="ce797-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce797-117">-DefaultProfile</span></span>
<span data-ttu-id="ce797-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce797-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce797-119">-Location</span><span class="sxs-lookup"><span data-stu-id="ce797-119">-Location</span></span>
<span data-ttu-id="ce797-120">Standort des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="ce797-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce797-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="ce797-121">-TypeName</span></span>
<span data-ttu-id="ce797-122">Name des Cognitive Services-Kontotyps.</span><span class="sxs-lookup"><span data-stu-id="ce797-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce797-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce797-123">CommonParameters</span></span>
<span data-ttu-id="ce797-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce797-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce797-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce797-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce797-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce797-126">INPUTS</span></span>

### <span data-ttu-id="ce797-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ce797-127">System.String</span></span>

## <span data-ttu-id="ce797-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce797-128">OUTPUTS</span></span>

### <span data-ttu-id="ce797-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ce797-129">System.String[]</span></span>

### <span data-ttu-id="ce797-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ce797-130">System.String</span></span>

## <span data-ttu-id="ce797-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ce797-131">NOTES</span></span>

## <span data-ttu-id="ce797-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ce797-132">RELATED LINKS</span></span>
