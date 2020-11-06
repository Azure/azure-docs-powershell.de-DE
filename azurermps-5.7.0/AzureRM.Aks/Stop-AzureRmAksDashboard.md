---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/stop-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
ms.openlocfilehash: 4ec1c8c2788469ffd377127bc58f657c817434a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500650"
---
# <span data-ttu-id="9c27b-101">Stop-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="9c27b-101">Stop-AzureRmAksDashboard</span></span>

## <span data-ttu-id="9c27b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c27b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c27b-103">Beenden Sie den Kubectl-SSH-Tunnel, der in Start-AzureRmKubernetesDashboard erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9c27b-103">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c27b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c27b-104">SYNTAX</span></span>

```
Stop-AzureRmAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c27b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c27b-105">DESCRIPTION</span></span>
<span data-ttu-id="9c27b-106">Beenden Sie den Kubectl-SSH-Tunnel, der in Start-AzureRmKubernetesDashboard erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9c27b-106">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="9c27b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c27b-107">EXAMPLES</span></span>

### <span data-ttu-id="9c27b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9c27b-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmKubernetesDashboard
```

<span data-ttu-id="9c27b-109">Beendet die vorhandene SSH-Tunnel Einrichtung durch Ausführen von Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="9c27b-109">Stops the existing SSH tunnel setup by executing Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="9c27b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c27b-110">PARAMETERS</span></span>

### <span data-ttu-id="9c27b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c27b-111">-DefaultProfile</span></span>
<span data-ttu-id="9c27b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c27b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c27b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c27b-113">-PassThru</span></span>
<span data-ttu-id="9c27b-114">Gibt "true" zurück, wenn der SSH-Tunnel geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9c27b-114">Returns true if SSH tunnel is closed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c27b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c27b-115">CommonParameters</span></span>
<span data-ttu-id="9c27b-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c27b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c27b-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c27b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c27b-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c27b-118">INPUTS</span></span>

### <span data-ttu-id="9c27b-119">Keine</span><span class="sxs-lookup"><span data-stu-id="9c27b-119">None</span></span>

## <span data-ttu-id="9c27b-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c27b-120">OUTPUTS</span></span>

### <span data-ttu-id="9c27b-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c27b-121">System.Boolean</span></span>

## <span data-ttu-id="9c27b-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c27b-122">NOTES</span></span>

## <span data-ttu-id="9c27b-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c27b-123">RELATED LINKS</span></span>
