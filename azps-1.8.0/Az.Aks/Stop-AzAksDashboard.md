---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 4d4e2a86bfa2974cabcc4208f7a314019f5804e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650444"
---
# <span data-ttu-id="cf74c-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="cf74c-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="cf74c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf74c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf74c-103">Beenden Sie den Kubectl-SSH-Tunnel, der in Start-AzKubernetesDashboard erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cf74c-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="cf74c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf74c-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf74c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf74c-105">DESCRIPTION</span></span>
<span data-ttu-id="cf74c-106">Beenden Sie den Kubectl-SSH-Tunnel, der in Start-AzKubernetesDashboard erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cf74c-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="cf74c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf74c-107">EXAMPLES</span></span>

### <span data-ttu-id="cf74c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cf74c-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="cf74c-109">Beendet die vorhandene SSH-Tunnel Einrichtung durch Ausführen von Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="cf74c-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="cf74c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf74c-110">PARAMETERS</span></span>

### <span data-ttu-id="cf74c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf74c-111">-DefaultProfile</span></span>
<span data-ttu-id="cf74c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf74c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf74c-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf74c-113">-PassThru</span></span>
<span data-ttu-id="cf74c-114">Gibt "true" zurück, wenn der SSH-Tunnel geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cf74c-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="cf74c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf74c-115">CommonParameters</span></span>
<span data-ttu-id="cf74c-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf74c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf74c-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf74c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf74c-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf74c-118">INPUTS</span></span>

### <span data-ttu-id="cf74c-119">Keine</span><span class="sxs-lookup"><span data-stu-id="cf74c-119">None</span></span>

## <span data-ttu-id="cf74c-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf74c-120">OUTPUTS</span></span>

### <span data-ttu-id="cf74c-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf74c-121">System.Boolean</span></span>

## <span data-ttu-id="cf74c-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf74c-122">NOTES</span></span>

## <span data-ttu-id="cf74c-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf74c-123">RELATED LINKS</span></span>
