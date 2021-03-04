---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: 3116ee67b55df50d4dc79df2ee3faef3823878b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935883"
---
# <span data-ttu-id="315c6-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="315c6-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="315c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="315c6-102">SYNOPSIS</span></span>
<span data-ttu-id="315c6-103">Generiert Registrierungsschlüssel für ein Automatisierungskonto neu.</span><span class="sxs-lookup"><span data-stu-id="315c6-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="315c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="315c6-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="315c6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="315c6-105">DESCRIPTION</span></span>
<span data-ttu-id="315c6-106">Das **Cmdlet New-AzAutomationKey** generiert registrierungsschlüssel für ein Azure Automation-Konto neu.</span><span class="sxs-lookup"><span data-stu-id="315c6-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="315c6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="315c6-107">EXAMPLES</span></span>

### <span data-ttu-id="315c6-108">Beispiel 1: Neuerieren eines Schlüssels für ein Automatisierungskonto</span><span class="sxs-lookup"><span data-stu-id="315c6-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="315c6-109">Mit diesem Befehl wird der Primärschlüssel für das Azure-Automatisierungskonto mit dem Namen AutomationAccount01 in der Ressourcengruppe "ResourceGroup01" neu generiert.</span><span class="sxs-lookup"><span data-stu-id="315c6-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="315c6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="315c6-110">PARAMETERS</span></span>

### <span data-ttu-id="315c6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="315c6-111">-AutomationAccountName</span></span>
<span data-ttu-id="315c6-112">Gibt den Namen eines Automatisierungskontos an, für das dieses Cmdlet Schlüssel neu generiert.</span><span class="sxs-lookup"><span data-stu-id="315c6-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="315c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315c6-113">-DefaultProfile</span></span>
<span data-ttu-id="315c6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="315c6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="315c6-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="315c6-115">-KeyType</span></span>
<span data-ttu-id="315c6-116">Gibt den Typ des Agentregistrierungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="315c6-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="315c6-117">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="315c6-117">Valid values are:</span></span> 
- <span data-ttu-id="315c6-118">Primär</span><span class="sxs-lookup"><span data-stu-id="315c6-118">Primary</span></span> 
- <span data-ttu-id="315c6-119">Sekundär</span><span class="sxs-lookup"><span data-stu-id="315c6-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="315c6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="315c6-120">-ResourceGroupName</span></span>
<span data-ttu-id="315c6-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="315c6-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="315c6-122">Dieses Cmdlet generiert Schlüssel für ein Automatisierungskonto in der Ressourcengruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="315c6-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="315c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315c6-123">CommonParameters</span></span>
<span data-ttu-id="315c6-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="315c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315c6-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="315c6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315c6-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="315c6-126">INPUTS</span></span>

### <span data-ttu-id="315c6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="315c6-127">System.String</span></span>

## <span data-ttu-id="315c6-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="315c6-128">OUTPUTS</span></span>

### <span data-ttu-id="315c6-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="315c6-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="315c6-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="315c6-130">NOTES</span></span>

## <span data-ttu-id="315c6-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="315c6-131">RELATED LINKS</span></span>
