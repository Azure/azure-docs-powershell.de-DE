---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 71f044dcce4944960d10fe2946b48c04354b8256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657949"
---
# <span data-ttu-id="2379e-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="2379e-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="2379e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2379e-102">SYNOPSIS</span></span>
<span data-ttu-id="2379e-103">Ändert den Wert eines Felds in einer Automatisierungs Verbindung.</span><span class="sxs-lookup"><span data-stu-id="2379e-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="2379e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2379e-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2379e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2379e-105">DESCRIPTION</span></span>
<span data-ttu-id="2379e-106">Das Cmdlet " **Satz-AzAutomationConnectionFieldValue** " ändert den Wert eines Felds in einer Verbindung in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="2379e-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="2379e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2379e-107">EXAMPLES</span></span>

### <span data-ttu-id="2379e-108">Beispiel 1: Ändern eines Feld Werts in einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="2379e-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="2379e-109">Dieser Befehl ändert die Abonnement-ID für die Azure-Verbindung mit dem Namen ContosoConnection im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="2379e-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="2379e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2379e-110">PARAMETERS</span></span>

### <span data-ttu-id="2379e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2379e-111">-AutomationAccountName</span></span>
<span data-ttu-id="2379e-112">Gibt den Namen des Automatisierungs Kontos an, für das mit diesem Cmdlet ein Feld in einer Verbindung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2379e-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="2379e-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="2379e-113">-ConnectionFieldName</span></span>
<span data-ttu-id="2379e-114">Gibt einen Namen für das Feld an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2379e-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2379e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2379e-115">-DefaultProfile</span></span>
<span data-ttu-id="2379e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2379e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2379e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2379e-117">-Name</span></span>
<span data-ttu-id="2379e-118">Gibt einen Namen für die Verbindung an, für die dieses Cmdlet ein Feld geändert hat.</span><span class="sxs-lookup"><span data-stu-id="2379e-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="2379e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2379e-119">-ResourceGroupName</span></span>
<span data-ttu-id="2379e-120">Gibt den Namen der Ressourcengruppe an, für die mit diesem Cmdlet ein Feld in einer Verbindung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2379e-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="2379e-121">-Wert</span><span class="sxs-lookup"><span data-stu-id="2379e-121">-Value</span></span>
<span data-ttu-id="2379e-122">Gibt einen Wert an, der im Verbindungsfeld geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2379e-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2379e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2379e-123">CommonParameters</span></span>
<span data-ttu-id="2379e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2379e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2379e-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2379e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2379e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2379e-126">INPUTS</span></span>

### <span data-ttu-id="2379e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2379e-127">System.String</span></span>

### <span data-ttu-id="2379e-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="2379e-128">System.Object</span></span>

## <span data-ttu-id="2379e-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2379e-129">OUTPUTS</span></span>

### <span data-ttu-id="2379e-130">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="2379e-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="2379e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2379e-131">NOTES</span></span>

## <span data-ttu-id="2379e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2379e-132">RELATED LINKS</span></span>

[<span data-ttu-id="2379e-133">Neu – AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="2379e-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


