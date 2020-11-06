---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: c7a4a34e3969f209bcd6fcaae46ed93cd316aba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479634"
---
# <span data-ttu-id="f1a6d-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="f1a6d-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="f1a6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a6d-103">Aktiviert oder deaktiviert das angegebene Intelligence Pack.</span><span class="sxs-lookup"><span data-stu-id="f1a6d-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1a6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1a6d-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1a6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a6d-106">Das Cmdlet " **Set-AzureRmOperationalInsightsIntelligencePack** " aktiviert das angegebene Intelligence Pack, wenn *Enabled* auf "$true" festgelegt ist und deaktiviert ist, wenn " *Enabled* " auf "$false" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f1a6d-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="f1a6d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1a6d-107">EXAMPLES</span></span>

### <span data-ttu-id="f1a6d-108">Beispiel 1: Einrichten von Intelligence Packs</span><span class="sxs-lookup"><span data-stu-id="f1a6d-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="f1a6d-109">Mit diesem Befehl wird das angegebene Intelligence Pack aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1a6d-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="f1a6d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1a6d-110">PARAMETERS</span></span>

### <span data-ttu-id="f1a6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a6d-111">-DefaultProfile</span></span>
<span data-ttu-id="f1a6d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f1a6d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1a6d-113">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="f1a6d-113">-Enabled</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a6d-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="f1a6d-114">-IntelligencePackName</span></span>
<span data-ttu-id="f1a6d-115">Gibt den Namen des Intelligence-Pakets an.</span><span class="sxs-lookup"><span data-stu-id="f1a6d-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a6d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a6d-116">-ResourceGroupName</span></span>
<span data-ttu-id="f1a6d-117">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f1a6d-117">Specifies the resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a6d-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1a6d-118">-WorkspaceName</span></span>
<span data-ttu-id="f1a6d-119">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="f1a6d-119">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a6d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a6d-120">CommonParameters</span></span>
<span data-ttu-id="f1a6d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a6d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a6d-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a6d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a6d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1a6d-123">INPUTS</span></span>

### <span data-ttu-id="f1a6d-124">Keine</span><span class="sxs-lookup"><span data-stu-id="f1a6d-124">None</span></span>
<span data-ttu-id="f1a6d-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f1a6d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1a6d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1a6d-126">OUTPUTS</span></span>

## <span data-ttu-id="f1a6d-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1a6d-127">NOTES</span></span>

## <span data-ttu-id="f1a6d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1a6d-128">RELATED LINKS</span></span>

[<span data-ttu-id="f1a6d-129">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="f1a6d-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


