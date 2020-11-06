---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/get-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
ms.openlocfilehash: d0140af9d5345e9f3f68c212ae43403fc0f64280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482494"
---
# <span data-ttu-id="158dd-101">Get-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="158dd-101">Get-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="158dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="158dd-102">SYNOPSIS</span></span>
<span data-ttu-id="158dd-103">Abrufen oder Auflisten des Azure-Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="158dd-103">Get or list Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="158dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="158dd-104">SYNTAX</span></span>

### <span data-ttu-id="158dd-105">ListDevSpacesControllerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="158dd-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzureRmDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="158dd-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="158dd-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="158dd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="158dd-107">DESCRIPTION</span></span>
<span data-ttu-id="158dd-108">Abrufen oder Auflisten des Azure-Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="158dd-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="158dd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="158dd-109">EXAMPLES</span></span>

### <span data-ttu-id="158dd-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="158dd-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="158dd-111">Auflisten aller Controller in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="158dd-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="158dd-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="158dd-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="158dd-113">Besorgen Sie sich ein-Controller in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="158dd-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="158dd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="158dd-114">PARAMETERS</span></span>

### <span data-ttu-id="158dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158dd-115">-DefaultProfile</span></span>
<span data-ttu-id="158dd-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="158dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="158dd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="158dd-117">-Name</span></span>
<span data-ttu-id="158dd-118">Name des Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="158dd-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="158dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="158dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="158dd-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="158dd-120">Resource group name</span></span>

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

### <span data-ttu-id="158dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158dd-121">CommonParameters</span></span>
<span data-ttu-id="158dd-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="158dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158dd-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="158dd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158dd-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="158dd-124">INPUTS</span></span>

### <span data-ttu-id="158dd-125">Keine</span><span class="sxs-lookup"><span data-stu-id="158dd-125">None</span></span>

## <span data-ttu-id="158dd-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="158dd-126">OUTPUTS</span></span>

### <span data-ttu-id="158dd-127">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="158dd-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="158dd-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="158dd-128">NOTES</span></span>

## <span data-ttu-id="158dd-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="158dd-129">RELATED LINKS</span></span>
