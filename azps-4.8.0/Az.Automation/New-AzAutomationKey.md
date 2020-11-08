---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008141"
---
# <span data-ttu-id="54234-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="54234-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="54234-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54234-102">SYNOPSIS</span></span>
<span data-ttu-id="54234-103">Regeneriert Registrierungsschlüssel für ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="54234-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="54234-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54234-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54234-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54234-105">DESCRIPTION</span></span>
<span data-ttu-id="54234-106">Das Cmdlet **New-AzAutomationKey** generiert Registrierungsschlüssel für ein Azure Automation-Konto neu.</span><span class="sxs-lookup"><span data-stu-id="54234-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="54234-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54234-107">EXAMPLES</span></span>

### <span data-ttu-id="54234-108">Beispiel 1: Erneutes Generieren eines Schlüssels für ein Automatisierungs Konto</span><span class="sxs-lookup"><span data-stu-id="54234-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="54234-109">Mit diesem Befehl wird der Primärschlüssel für das Azure Automation-Konto mit dem Namen AutomationAccount01 in der Ressourcengruppe mit dem Namen ResourceGroup01 neu generiert.</span><span class="sxs-lookup"><span data-stu-id="54234-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="54234-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="54234-110">PARAMETERS</span></span>

### <span data-ttu-id="54234-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="54234-111">-AutomationAccountName</span></span>
<span data-ttu-id="54234-112">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet Schlüssel neu generiert.</span><span class="sxs-lookup"><span data-stu-id="54234-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="54234-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54234-113">-DefaultProfile</span></span>
<span data-ttu-id="54234-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="54234-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54234-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="54234-115">-KeyType</span></span>
<span data-ttu-id="54234-116">Gibt den Typ des Agenten Registrierungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="54234-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="54234-117">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="54234-117">Valid values are:</span></span> 
- <span data-ttu-id="54234-118">Primär</span><span class="sxs-lookup"><span data-stu-id="54234-118">Primary</span></span> 
- <span data-ttu-id="54234-119">Sekundär</span><span class="sxs-lookup"><span data-stu-id="54234-119">Secondary</span></span>

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

### <span data-ttu-id="54234-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54234-120">-ResourceGroupName</span></span>
<span data-ttu-id="54234-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="54234-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="54234-122">Mit diesem Cmdlet werden die Schlüssel für ein Automatisierungs Konto in der Ressourcengruppe, die dieser Parameter angibt, erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="54234-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="54234-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54234-123">CommonParameters</span></span>
<span data-ttu-id="54234-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54234-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54234-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54234-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54234-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54234-126">INPUTS</span></span>

### <span data-ttu-id="54234-127">System. String</span><span class="sxs-lookup"><span data-stu-id="54234-127">System.String</span></span>

## <span data-ttu-id="54234-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54234-128">OUTPUTS</span></span>

### <span data-ttu-id="54234-129">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="54234-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="54234-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="54234-130">NOTES</span></span>

## <span data-ttu-id="54234-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54234-131">RELATED LINKS</span></span>
