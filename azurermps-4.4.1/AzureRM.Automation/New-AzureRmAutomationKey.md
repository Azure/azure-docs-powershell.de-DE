---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 3b29d1b07ab0c11f42f1a7d4d9326ae19f6b79f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503278"
---
# <span data-ttu-id="e1bf1-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="e1bf1-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="e1bf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bf1-103">Regeneriert Registrierungsschlüssel für ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1bf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1bf1-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1bf1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1bf1-105">DESCRIPTION</span></span>
<span data-ttu-id="e1bf1-106">Das Cmdlet **New-AzureRmAutomationKey** generiert Registrierungsschlüssel für ein Azure Automation-Konto neu.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="e1bf1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1bf1-107">EXAMPLES</span></span>

### <span data-ttu-id="e1bf1-108">Beispiel 1: Erneutes Generieren eines Schlüssels für ein Automatisierungs Konto</span><span class="sxs-lookup"><span data-stu-id="e1bf1-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="e1bf1-109">Mit diesem Befehl wird der Primärschlüssel für das Azure Automation-Konto mit dem Namen AutomationAccount01 in der Ressourcengruppe mit dem Namen ResourceGroup01 neu generiert.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="e1bf1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1bf1-110">PARAMETERS</span></span>

### <span data-ttu-id="e1bf1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e1bf1-111">-AutomationAccountName</span></span>
<span data-ttu-id="e1bf1-112">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet Schlüssel neu generiert.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="e1bf1-113">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e1bf1-113">-KeyType</span></span>
<span data-ttu-id="e1bf1-114">Gibt den Typ des Agenten Registrierungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-114">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="e1bf1-115">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="e1bf1-115">Valid values are:</span></span> 

- <span data-ttu-id="e1bf1-116">Primär</span><span class="sxs-lookup"><span data-stu-id="e1bf1-116">Primary</span></span> 
- <span data-ttu-id="e1bf1-117">Sekundär</span><span class="sxs-lookup"><span data-stu-id="e1bf1-117">Secondary</span></span>

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

### <span data-ttu-id="e1bf1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1bf1-118">-ResourceGroupName</span></span>
<span data-ttu-id="e1bf1-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e1bf1-120">Mit diesem Cmdlet werden die Schlüssel für ein Automatisierungs Konto in der Ressourcengruppe, die dieser Parameter angibt, erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-120">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1bf1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bf1-121">-DefaultProfile</span></span>
<span data-ttu-id="e1bf1-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1bf1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bf1-123">CommonParameters</span></span>
<span data-ttu-id="e1bf1-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bf1-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1bf1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bf1-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1bf1-126">INPUTS</span></span>

## <span data-ttu-id="e1bf1-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1bf1-127">OUTPUTS</span></span>

### <span data-ttu-id="e1bf1-128">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="e1bf1-128">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="e1bf1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1bf1-129">NOTES</span></span>

## <span data-ttu-id="e1bf1-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1bf1-130">RELATED LINKS</span></span>

