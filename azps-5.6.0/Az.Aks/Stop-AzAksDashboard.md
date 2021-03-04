---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 633173a0ce8814ee2af9300be5b1cfc19bdf9a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930432"
---
# <span data-ttu-id="43a02-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="43a02-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="43a02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43a02-102">SYNOPSIS</span></span>
<span data-ttu-id="43a02-103">Beenden Sie den in Start-AzKubernetesDashboard erstellten Kubectl-SSH-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="43a02-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="43a02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43a02-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43a02-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43a02-105">DESCRIPTION</span></span>
<span data-ttu-id="43a02-106">Beenden Sie den in Start-AzKubernetesDashboard erstellten Kubectl-SSH-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="43a02-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="43a02-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43a02-107">EXAMPLES</span></span>

### <span data-ttu-id="43a02-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43a02-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="43a02-109">Beendet das vorhandene SSH-Tunnel-Setup, indem Start-AzKubernetesDashboard ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43a02-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="43a02-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43a02-110">PARAMETERS</span></span>

### <span data-ttu-id="43a02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a02-111">-DefaultProfile</span></span>
<span data-ttu-id="43a02-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43a02-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43a02-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43a02-113">-PassThru</span></span>
<span data-ttu-id="43a02-114">Gibt "true" zurück, wenn der SSH-Tunnel geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="43a02-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="43a02-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a02-115">CommonParameters</span></span>
<span data-ttu-id="43a02-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a02-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a02-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43a02-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a02-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43a02-118">INPUTS</span></span>

### <span data-ttu-id="43a02-119">Keine</span><span class="sxs-lookup"><span data-stu-id="43a02-119">None</span></span>

## <span data-ttu-id="43a02-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43a02-120">OUTPUTS</span></span>

### <span data-ttu-id="43a02-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43a02-121">System.Boolean</span></span>

## <span data-ttu-id="43a02-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="43a02-122">NOTES</span></span>

## <span data-ttu-id="43a02-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="43a02-123">RELATED LINKS</span></span>
