---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 75c69c96b82cf71aa71d4ac89bb10c064af1f4f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166184"
---
# <span data-ttu-id="07ba4-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="07ba4-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="07ba4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="07ba4-103">Ruft die freigegebenen Schlüssel für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="07ba4-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="07ba4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07ba4-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07ba4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="07ba4-106">Das Cmdlet " **Get-AzOperationalInsightsWorkspaceSharedKey** " listet die freigegebenen Schlüssel für einen Arbeitsbereich auf.</span><span class="sxs-lookup"><span data-stu-id="07ba4-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="07ba4-107">Die Schlüssel werden verwendet, um operative Einblicke-Agents mit dem Arbeitsbereich zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="07ba4-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="07ba4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07ba4-108">EXAMPLES</span></span>

### <span data-ttu-id="07ba4-109">Beispiel 1: Abrufen von freigegebenen Schlüsseln nach Arbeitsbereichsnamen</span><span class="sxs-lookup"><span data-stu-id="07ba4-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="07ba4-110">Dieser Befehl ruft die freigegebenen Schlüssel für den Arbeitsbereich mit dem Namen "myworkspace" in der Ressourcengruppe mit dem Namen ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="07ba4-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="07ba4-111">Beispiel 2: Abrufen von freigegebenen Schlüsseln mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="07ba4-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="07ba4-112">Dieser Befehl ruft den Arbeitsbereich mit dem Namen "myworkspace" mithilfe des Get-AzOperationalInsightsWorkspace-Cmdlets ab und übergibt dann den Arbeitsbereich an das Cmdlet " **Get-AzOperationalInsightsWorkspaceSharedKey** ".</span><span class="sxs-lookup"><span data-stu-id="07ba4-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="07ba4-113">Der Befehl ruft die freigegebenen Schlüssel für diesen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="07ba4-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="07ba4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="07ba4-114">PARAMETERS</span></span>

### <span data-ttu-id="07ba4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ba4-115">-DefaultProfile</span></span>
<span data-ttu-id="07ba4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="07ba4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07ba4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="07ba4-117">-Name</span></span>
<span data-ttu-id="07ba4-118">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="07ba4-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ba4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ba4-119">-ResourceGroupName</span></span>
<span data-ttu-id="07ba4-120">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="07ba4-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ba4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ba4-121">CommonParameters</span></span>
<span data-ttu-id="07ba4-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ba4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ba4-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ba4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ba4-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07ba4-124">INPUTS</span></span>

### <span data-ttu-id="07ba4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="07ba4-125">System.String</span></span>

## <span data-ttu-id="07ba4-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07ba4-126">OUTPUTS</span></span>

### <span data-ttu-id="07ba4-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="07ba4-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="07ba4-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="07ba4-128">NOTES</span></span>

## <span data-ttu-id="07ba4-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07ba4-129">RELATED LINKS</span></span>

[<span data-ttu-id="07ba4-130">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="07ba4-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="07ba4-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="07ba4-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


