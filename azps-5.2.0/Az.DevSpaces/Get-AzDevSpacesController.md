---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292259"
---
# <span data-ttu-id="78855-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="78855-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="78855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78855-102">SYNOPSIS</span></span>
<span data-ttu-id="78855-103">Holen Sie sich den Azure DevSpaces-Controller, oder listen Sie diese auf.</span><span class="sxs-lookup"><span data-stu-id="78855-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="78855-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78855-104">SYNTAX</span></span>

### <span data-ttu-id="78855-105">ListDevSpacesControllerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="78855-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78855-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78855-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78855-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78855-107">DESCRIPTION</span></span>
<span data-ttu-id="78855-108">Holen Sie sich den Azure DevSpaces-Controller, oder listen Sie diese auf.</span><span class="sxs-lookup"><span data-stu-id="78855-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="78855-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78855-109">EXAMPLES</span></span>

### <span data-ttu-id="78855-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78855-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="78855-111">Listen Sie alle Controller in einem Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="78855-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="78855-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="78855-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="78855-113">Holen Sie sich die DevSpaces-Controller in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78855-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="78855-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78855-114">PARAMETERS</span></span>

### <span data-ttu-id="78855-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78855-115">-DefaultProfile</span></span>
<span data-ttu-id="78855-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78855-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78855-117">-Name</span><span class="sxs-lookup"><span data-stu-id="78855-117">-Name</span></span>
<span data-ttu-id="78855-118">DevSpaces-Controllername.</span><span class="sxs-lookup"><span data-stu-id="78855-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="78855-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78855-119">-ResourceGroupName</span></span>
<span data-ttu-id="78855-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="78855-120">Resource group name</span></span>

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

### <span data-ttu-id="78855-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78855-121">CommonParameters</span></span>
<span data-ttu-id="78855-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78855-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78855-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78855-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78855-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78855-124">INPUTS</span></span>

### <span data-ttu-id="78855-125">Keine</span><span class="sxs-lookup"><span data-stu-id="78855-125">None</span></span>

## <span data-ttu-id="78855-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78855-126">OUTPUTS</span></span>

### <span data-ttu-id="78855-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="78855-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="78855-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="78855-128">NOTES</span></span>

## <span data-ttu-id="78855-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="78855-129">RELATED LINKS</span></span>
