---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009861"
---
# <span data-ttu-id="07f1b-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="07f1b-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="07f1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="07f1b-103">Abrufen oder Auflisten des Azure-Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="07f1b-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="07f1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07f1b-104">SYNTAX</span></span>

### <span data-ttu-id="07f1b-105">ListDevSpacesControllerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="07f1b-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07f1b-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f1b-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07f1b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07f1b-107">DESCRIPTION</span></span>
<span data-ttu-id="07f1b-108">Abrufen oder Auflisten des Azure-Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="07f1b-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="07f1b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07f1b-109">EXAMPLES</span></span>

### <span data-ttu-id="07f1b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07f1b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="07f1b-111">Auflisten aller Controller in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07f1b-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="07f1b-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="07f1b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="07f1b-113">Besorgen Sie sich ein-Controller in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07f1b-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="07f1b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="07f1b-114">PARAMETERS</span></span>

### <span data-ttu-id="07f1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f1b-115">-DefaultProfile</span></span>
<span data-ttu-id="07f1b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07f1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f1b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="07f1b-117">-Name</span></span>
<span data-ttu-id="07f1b-118">Name des Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="07f1b-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="07f1b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f1b-119">-ResourceGroupName</span></span>
<span data-ttu-id="07f1b-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="07f1b-120">Resource group name</span></span>

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

### <span data-ttu-id="07f1b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f1b-121">CommonParameters</span></span>
<span data-ttu-id="07f1b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f1b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f1b-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f1b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f1b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07f1b-124">INPUTS</span></span>

### <span data-ttu-id="07f1b-125">Keine</span><span class="sxs-lookup"><span data-stu-id="07f1b-125">None</span></span>

## <span data-ttu-id="07f1b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07f1b-126">OUTPUTS</span></span>

### <span data-ttu-id="07f1b-127">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="07f1b-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="07f1b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="07f1b-128">NOTES</span></span>

## <span data-ttu-id="07f1b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07f1b-129">RELATED LINKS</span></span>
