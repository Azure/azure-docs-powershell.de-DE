---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173662"
---
# <span data-ttu-id="97704-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="97704-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="97704-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97704-102">SYNOPSIS</span></span>
<span data-ttu-id="97704-103">Überprüft, ob ein Synapse Analytics-Arbeitsbereich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="97704-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="97704-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97704-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97704-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97704-105">DESCRIPTION</span></span>
<span data-ttu-id="97704-106">Das Cmdlet **Test-AzSynapseWorkspace** überprüft, ob ein Synapse Analytics-Arbeitsbereich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="97704-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="97704-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97704-107">EXAMPLES</span></span>

### <span data-ttu-id="97704-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97704-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="97704-109">Dieser Befehl überprüft, ob ein Synapse Analytics-Arbeitsbereich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="97704-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="97704-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="97704-110">PARAMETERS</span></span>

### <span data-ttu-id="97704-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97704-111">-DefaultProfile</span></span>
<span data-ttu-id="97704-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97704-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97704-113">-Name</span><span class="sxs-lookup"><span data-stu-id="97704-113">-Name</span></span>
<span data-ttu-id="97704-114">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="97704-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="97704-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97704-115">-ResourceGroupName</span></span>
<span data-ttu-id="97704-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="97704-116">Resource group name.</span></span>

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

### <span data-ttu-id="97704-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97704-117">CommonParameters</span></span>
<span data-ttu-id="97704-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97704-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97704-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97704-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97704-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97704-120">INPUTS</span></span>

### <span data-ttu-id="97704-121">Keine</span><span class="sxs-lookup"><span data-stu-id="97704-121">None</span></span>

## <span data-ttu-id="97704-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97704-122">OUTPUTS</span></span>

### <span data-ttu-id="97704-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="97704-123">System.Object</span></span>
## <span data-ttu-id="97704-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="97704-124">NOTES</span></span>

## <span data-ttu-id="97704-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97704-125">RELATED LINKS</span></span>
