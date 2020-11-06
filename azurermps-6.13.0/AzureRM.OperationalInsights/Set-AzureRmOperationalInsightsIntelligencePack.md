---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 0e8335476fc1cb511aaddb5294ea508832a04003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480221"
---
# <span data-ttu-id="5f2a0-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="5f2a0-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="5f2a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5f2a0-103">Aktiviert oder deaktiviert das angegebene Intelligence Pack.</span><span class="sxs-lookup"><span data-stu-id="5f2a0-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f2a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f2a0-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f2a0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f2a0-105">DESCRIPTION</span></span>
<span data-ttu-id="5f2a0-106">Das Cmdlet " **Set-AzureRmOperationalInsightsIntelligencePack** " aktiviert das angegebene Intelligence Pack, wenn *Enabled* auf "$true" festgelegt ist und deaktiviert ist, wenn " *Enabled* " auf "$false" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5f2a0-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="5f2a0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f2a0-107">EXAMPLES</span></span>

### <span data-ttu-id="5f2a0-108">Beispiel 1: Einrichten von Intelligence Packs</span><span class="sxs-lookup"><span data-stu-id="5f2a0-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="5f2a0-109">Mit diesem Befehl wird das angegebene Intelligence Pack aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5f2a0-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="5f2a0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f2a0-110">PARAMETERS</span></span>

### <span data-ttu-id="5f2a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f2a0-111">-DefaultProfile</span></span>
<span data-ttu-id="5f2a0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5f2a0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f2a0-113">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="5f2a0-113">-Enabled</span></span>
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

### <span data-ttu-id="5f2a0-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="5f2a0-114">-IntelligencePackName</span></span>
<span data-ttu-id="5f2a0-115">Gibt den Namen des Intelligence-Pakets an.</span><span class="sxs-lookup"><span data-stu-id="5f2a0-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="5f2a0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f2a0-116">-ResourceGroupName</span></span>
<span data-ttu-id="5f2a0-117">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5f2a0-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="5f2a0-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5f2a0-118">-WorkspaceName</span></span>
<span data-ttu-id="5f2a0-119">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="5f2a0-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="5f2a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f2a0-120">CommonParameters</span></span>
<span data-ttu-id="5f2a0-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f2a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f2a0-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f2a0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f2a0-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f2a0-123">INPUTS</span></span>

### <span data-ttu-id="5f2a0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5f2a0-124">System.String</span></span>

### <span data-ttu-id="5f2a0-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f2a0-125">System.Boolean</span></span>

## <span data-ttu-id="5f2a0-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f2a0-126">OUTPUTS</span></span>

### <span data-ttu-id="5f2a0-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="5f2a0-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="5f2a0-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f2a0-128">NOTES</span></span>

## <span data-ttu-id="5f2a0-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f2a0-129">RELATED LINKS</span></span>

[<span data-ttu-id="5f2a0-130">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="5f2a0-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


