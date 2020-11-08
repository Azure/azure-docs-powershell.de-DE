---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178706"
---
# <span data-ttu-id="00dbb-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="00dbb-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="00dbb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="00dbb-103">Listen Sie gelöschte Arbeitsbereiche auf.</span><span class="sxs-lookup"><span data-stu-id="00dbb-103">List deleted workspaces.</span></span>

## <span data-ttu-id="00dbb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00dbb-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00dbb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00dbb-105">DESCRIPTION</span></span>
<span data-ttu-id="00dbb-106">Listen Sie gelöschte Arbeitsbereiche auf.</span><span class="sxs-lookup"><span data-stu-id="00dbb-106">List deleted workspaces.</span></span>

## <span data-ttu-id="00dbb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00dbb-107">EXAMPLES</span></span>

### <span data-ttu-id="00dbb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00dbb-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="00dbb-109">Listen Sie gelöschte Arbeitsbereiche auf.</span><span class="sxs-lookup"><span data-stu-id="00dbb-109">List deleted workspaces.</span></span>

## <span data-ttu-id="00dbb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="00dbb-110">PARAMETERS</span></span>

### <span data-ttu-id="00dbb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00dbb-111">-DefaultProfile</span></span>
<span data-ttu-id="00dbb-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00dbb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00dbb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00dbb-113">-ResourceGroupName</span></span>
<span data-ttu-id="00dbb-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="00dbb-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00dbb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00dbb-115">CommonParameters</span></span>
<span data-ttu-id="00dbb-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00dbb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00dbb-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00dbb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00dbb-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00dbb-118">INPUTS</span></span>

### <span data-ttu-id="00dbb-119">System. String</span><span class="sxs-lookup"><span data-stu-id="00dbb-119">System.String</span></span>

## <span data-ttu-id="00dbb-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00dbb-120">OUTPUTS</span></span>

### <span data-ttu-id="00dbb-121">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="00dbb-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="00dbb-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="00dbb-122">NOTES</span></span>

## <span data-ttu-id="00dbb-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00dbb-123">RELATED LINKS</span></span>
