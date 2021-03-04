---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: dd7ba99632cfef493fe3202b2402a938b11fa807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922995"
---
# <span data-ttu-id="9f6da-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="9f6da-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="9f6da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f6da-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6da-103">Azure DevSpaces-Controller erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="9f6da-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="9f6da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f6da-104">SYNTAX</span></span>

### <span data-ttu-id="9f6da-105">ListDevSpacesControllerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f6da-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f6da-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f6da-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f6da-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f6da-107">DESCRIPTION</span></span>
<span data-ttu-id="9f6da-108">Azure DevSpaces-Controller erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="9f6da-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="9f6da-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f6da-109">EXAMPLES</span></span>

### <span data-ttu-id="9f6da-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f6da-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="9f6da-111">Listen Sie alle Controller in einem Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="9f6da-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="9f6da-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9f6da-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="9f6da-113">Holen Sie sich einen DevSpaces-Controller in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f6da-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="9f6da-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f6da-114">PARAMETERS</span></span>

### <span data-ttu-id="9f6da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6da-115">-DefaultProfile</span></span>
<span data-ttu-id="9f6da-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f6da-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f6da-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9f6da-117">-Name</span></span>
<span data-ttu-id="9f6da-118">DevSpaces-Controllername.</span><span class="sxs-lookup"><span data-stu-id="9f6da-118">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6da-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f6da-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f6da-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="9f6da-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ListDevSpacesControllerParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6da-121">CommonParameters</span></span>
<span data-ttu-id="9f6da-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6da-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f6da-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6da-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f6da-124">INPUTS</span></span>

### <span data-ttu-id="9f6da-125">Keine</span><span class="sxs-lookup"><span data-stu-id="9f6da-125">None</span></span>

## <span data-ttu-id="9f6da-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f6da-126">OUTPUTS</span></span>

### <span data-ttu-id="9f6da-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="9f6da-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="9f6da-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9f6da-128">NOTES</span></span>

## <span data-ttu-id="9f6da-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9f6da-129">RELATED LINKS</span></span>
