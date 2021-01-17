---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469252"
---
# <span data-ttu-id="c9b3a-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c9b3a-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="c9b3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b3a-103">Überprüft, ob ein Synapse Analytics-Arbeitsbereich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="c9b3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9b3a-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9b3a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9b3a-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b3a-106">Das **Cmdlet "Test-AzSynapseWorkspace"** sucht nach dem Vorhandensein eines Synapse Analytics-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="c9b3a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c9b3a-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b3a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c9b3a-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="c9b3a-109">Mit diesem Befehl wird überprüft, ob ein Synapse Analytics-Arbeitsbereich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="c9b3a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9b3a-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b3a-111">-DefaultProfile</span></span>
<span data-ttu-id="c9b3a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b3a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c9b3a-113">-Name</span></span>
<span data-ttu-id="c9b3a-114">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-114">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b3a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b3a-115">-ResourceGroupName</span></span>
<span data-ttu-id="c9b3a-116">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b3a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b3a-117">CommonParameters</span></span>
<span data-ttu-id="c9b3a-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b3a-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9b3a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b3a-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c9b3a-120">INPUTS</span></span>

### <span data-ttu-id="c9b3a-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c9b3a-121">None</span></span>

## <span data-ttu-id="c9b3a-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c9b3a-122">OUTPUTS</span></span>

### <span data-ttu-id="c9b3a-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="c9b3a-123">System.Object</span></span>
## <span data-ttu-id="c9b3a-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c9b3a-124">NOTES</span></span>

## <span data-ttu-id="c9b3a-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c9b3a-125">RELATED LINKS</span></span>
