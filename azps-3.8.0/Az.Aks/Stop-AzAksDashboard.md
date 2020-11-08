---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: f8d2331852fe60220b62313e007f2b5f3727466d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995914"
---
# <span data-ttu-id="e85b6-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="e85b6-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="e85b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e85b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e85b6-103">Beenden Sie den Kubectl-SSH-Tunnel, der in Start-AzKubernetesDashboard erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e85b6-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="e85b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e85b6-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e85b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e85b6-105">DESCRIPTION</span></span>
<span data-ttu-id="e85b6-106">Beenden Sie den Kubectl-SSH-Tunnel, der in Start-AzKubernetesDashboard erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e85b6-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="e85b6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e85b6-107">EXAMPLES</span></span>

### <span data-ttu-id="e85b6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e85b6-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="e85b6-109">Beendet die vorhandene SSH-Tunnel Einrichtung durch Ausführen von Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="e85b6-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="e85b6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e85b6-110">PARAMETERS</span></span>

### <span data-ttu-id="e85b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85b6-111">-DefaultProfile</span></span>
<span data-ttu-id="e85b6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e85b6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e85b6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e85b6-113">-PassThru</span></span>
<span data-ttu-id="e85b6-114">Gibt "true" zurück, wenn der SSH-Tunnel geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e85b6-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="e85b6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85b6-115">CommonParameters</span></span>
<span data-ttu-id="e85b6-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e85b6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85b6-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e85b6-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85b6-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e85b6-118">INPUTS</span></span>

### <span data-ttu-id="e85b6-119">Keine</span><span class="sxs-lookup"><span data-stu-id="e85b6-119">None</span></span>

## <span data-ttu-id="e85b6-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e85b6-120">OUTPUTS</span></span>

### <span data-ttu-id="e85b6-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e85b6-121">System.Boolean</span></span>

## <span data-ttu-id="e85b6-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="e85b6-122">NOTES</span></span>

## <span data-ttu-id="e85b6-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e85b6-123">RELATED LINKS</span></span>
