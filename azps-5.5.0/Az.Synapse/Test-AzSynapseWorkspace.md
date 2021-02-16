---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173516"
---
# <span data-ttu-id="1d403-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1d403-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="1d403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d403-102">SYNOPSIS</span></span>
<span data-ttu-id="1d403-103">Überprüft, ob ein Synapse Analytics-Arbeitsbereich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1d403-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="1d403-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d403-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d403-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d403-105">DESCRIPTION</span></span>
<span data-ttu-id="1d403-106">Das **Cmdlet "Test-AzSynapseWorkspace"** sucht nach dem Vorhandensein eines Synapse Analytics-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="1d403-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="1d403-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d403-107">EXAMPLES</span></span>

### <span data-ttu-id="1d403-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1d403-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="1d403-109">Mit diesem Befehl wird überprüft, ob ein Synapse Analytics-Arbeitsbereich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1d403-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="1d403-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d403-110">PARAMETERS</span></span>

### <span data-ttu-id="1d403-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d403-111">-DefaultProfile</span></span>
<span data-ttu-id="1d403-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d403-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d403-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1d403-113">-Name</span></span>
<span data-ttu-id="1d403-114">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="1d403-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1d403-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d403-115">-ResourceGroupName</span></span>
<span data-ttu-id="1d403-116">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="1d403-116">Resource group name.</span></span>

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

### <span data-ttu-id="1d403-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d403-117">CommonParameters</span></span>
<span data-ttu-id="1d403-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d403-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d403-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d403-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d403-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d403-120">INPUTS</span></span>

### <span data-ttu-id="1d403-121">Keine</span><span class="sxs-lookup"><span data-stu-id="1d403-121">None</span></span>

## <span data-ttu-id="1d403-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d403-122">OUTPUTS</span></span>

### <span data-ttu-id="1d403-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="1d403-123">System.Object</span></span>
## <span data-ttu-id="1d403-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d403-124">NOTES</span></span>

## <span data-ttu-id="1d403-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d403-125">RELATED LINKS</span></span>
