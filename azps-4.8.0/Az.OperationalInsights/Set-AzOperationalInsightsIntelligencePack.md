---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165071"
---
# <span data-ttu-id="a9f85-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="a9f85-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="a9f85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9f85-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f85-103">Aktiviert oder deaktiviert das angegebene Intelligence Pack.</span><span class="sxs-lookup"><span data-stu-id="a9f85-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="a9f85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9f85-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9f85-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9f85-105">DESCRIPTION</span></span>
<span data-ttu-id="a9f85-106">Das Cmdlet " **Set-AzOperationalInsightsIntelligencePack** " aktiviert das angegebene Intelligence Pack, wenn *Enabled* auf "$true" festgelegt ist und deaktiviert ist, wenn " *Enabled* " auf "$false" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a9f85-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="a9f85-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9f85-107">EXAMPLES</span></span>

### <span data-ttu-id="a9f85-108">Beispiel 1: Einrichten von Intelligence Packs</span><span class="sxs-lookup"><span data-stu-id="a9f85-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="a9f85-109">Mit diesem Befehl wird das angegebene Intelligence Pack aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a9f85-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="a9f85-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9f85-110">PARAMETERS</span></span>

### <span data-ttu-id="a9f85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f85-111">-DefaultProfile</span></span>
<span data-ttu-id="a9f85-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a9f85-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9f85-113">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="a9f85-113">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9f85-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="a9f85-114">-IntelligencePackName</span></span>
<span data-ttu-id="a9f85-115">Gibt den Namen des Intelligence-Pakets an.</span><span class="sxs-lookup"><span data-stu-id="a9f85-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9f85-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9f85-116">-ResourceGroupName</span></span>
<span data-ttu-id="a9f85-117">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a9f85-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="a9f85-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a9f85-118">-WorkspaceName</span></span>
<span data-ttu-id="a9f85-119">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="a9f85-119">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9f85-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f85-120">CommonParameters</span></span>
<span data-ttu-id="a9f85-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9f85-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f85-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9f85-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f85-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9f85-123">INPUTS</span></span>

### <span data-ttu-id="a9f85-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a9f85-124">System.String</span></span>

### <span data-ttu-id="a9f85-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9f85-125">System.Boolean</span></span>

## <span data-ttu-id="a9f85-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9f85-126">OUTPUTS</span></span>

### <span data-ttu-id="a9f85-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="a9f85-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="a9f85-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9f85-128">NOTES</span></span>

## <span data-ttu-id="a9f85-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9f85-129">RELATED LINKS</span></span>

[<span data-ttu-id="a9f85-130">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="a9f85-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


