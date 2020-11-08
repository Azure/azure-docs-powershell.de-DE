---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165383"
---
# <span data-ttu-id="a0be1-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="a0be1-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="a0be1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0be1-102">SYNOPSIS</span></span>
<span data-ttu-id="a0be1-103">Beenden Sie den Kubectl-SSH-Tunnel, der in Start-AzKubernetesDashboard erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a0be1-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="a0be1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0be1-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0be1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0be1-105">DESCRIPTION</span></span>
<span data-ttu-id="a0be1-106">Beenden Sie den Kubectl-SSH-Tunnel, der in Start-AzKubernetesDashboard erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a0be1-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="a0be1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0be1-107">EXAMPLES</span></span>

### <span data-ttu-id="a0be1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0be1-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="a0be1-109">Beendet die vorhandene SSH-Tunnel Einrichtung durch Ausführen von Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="a0be1-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="a0be1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0be1-110">PARAMETERS</span></span>

### <span data-ttu-id="a0be1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0be1-111">-DefaultProfile</span></span>
<span data-ttu-id="a0be1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0be1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0be1-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0be1-113">-PassThru</span></span>
<span data-ttu-id="a0be1-114">Gibt "true" zurück, wenn der SSH-Tunnel geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a0be1-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="a0be1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0be1-115">CommonParameters</span></span>
<span data-ttu-id="a0be1-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0be1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0be1-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0be1-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0be1-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0be1-118">INPUTS</span></span>

### <span data-ttu-id="a0be1-119">Keine</span><span class="sxs-lookup"><span data-stu-id="a0be1-119">None</span></span>

## <span data-ttu-id="a0be1-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0be1-120">OUTPUTS</span></span>

### <span data-ttu-id="a0be1-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0be1-121">System.Boolean</span></span>

## <span data-ttu-id="a0be1-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0be1-122">NOTES</span></span>

## <span data-ttu-id="a0be1-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0be1-123">RELATED LINKS</span></span>
