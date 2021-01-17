---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469111"
---
# <span data-ttu-id="11b55-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="11b55-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="11b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b55-102">SYNOPSIS</span></span>
<span data-ttu-id="11b55-103">Beenden Sie den in Start-AzAkaernetesDashboard erstellten Kubectl-SSH-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="11b55-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="11b55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11b55-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11b55-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11b55-105">DESCRIPTION</span></span>
<span data-ttu-id="11b55-106">Beenden Sie den in Start-AzAkaernetesDashboard erstellten Kubectl-SSH-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="11b55-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="11b55-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="11b55-107">EXAMPLES</span></span>

### <span data-ttu-id="11b55-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="11b55-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="11b55-109">Beendet das vorhandene Setup des SSH-Tunnels, indem "Start-AzAkaernetesDashboard" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11b55-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="11b55-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11b55-110">PARAMETERS</span></span>

### <span data-ttu-id="11b55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b55-111">-DefaultProfile</span></span>
<span data-ttu-id="11b55-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11b55-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11b55-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11b55-113">-PassThru</span></span>
<span data-ttu-id="11b55-114">Gibt "true" zurück, wenn der SSH-Tunnel geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="11b55-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="11b55-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b55-115">CommonParameters</span></span>
<span data-ttu-id="11b55-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b55-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b55-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11b55-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b55-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="11b55-118">INPUTS</span></span>

### <span data-ttu-id="11b55-119">Keine</span><span class="sxs-lookup"><span data-stu-id="11b55-119">None</span></span>

## <span data-ttu-id="11b55-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="11b55-120">OUTPUTS</span></span>

### <span data-ttu-id="11b55-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11b55-121">System.Boolean</span></span>

## <span data-ttu-id="11b55-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="11b55-122">NOTES</span></span>

## <span data-ttu-id="11b55-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="11b55-123">RELATED LINKS</span></span>
