---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 2df58153b2617a8ad62b0e46544128fa47a462b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373105"
---
# <span data-ttu-id="14c38-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="14c38-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="14c38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c38-102">SYNOPSIS</span></span>
<span data-ttu-id="14c38-103">Ändert den Wert eines Felds in einer Automatisierungsverbindung.</span><span class="sxs-lookup"><span data-stu-id="14c38-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="14c38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14c38-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14c38-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14c38-105">DESCRIPTION</span></span>
<span data-ttu-id="14c38-106">Das **Cmdlet "Set-AzAutomationConnectionFieldValue"** ändert den Wert eines Felds in einer Verbindung in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="14c38-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="14c38-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14c38-107">EXAMPLES</span></span>

### <span data-ttu-id="14c38-108">Beispiel 1: Ändern eines Feldwerts in einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="14c38-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="14c38-109">Mit diesem Befehl wird die Abonnement-ID für die Azure-Verbindung namens "ContosoConnection" im Automatisierungskonto namens "AutomationAccount01" geändert.</span><span class="sxs-lookup"><span data-stu-id="14c38-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="14c38-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14c38-110">PARAMETERS</span></span>

### <span data-ttu-id="14c38-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="14c38-111">-AutomationAccountName</span></span>
<span data-ttu-id="14c38-112">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet ein Feld in einer Verbindung ändert.</span><span class="sxs-lookup"><span data-stu-id="14c38-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="14c38-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="14c38-113">-ConnectionFieldName</span></span>
<span data-ttu-id="14c38-114">Gibt einen Namen für das Feld an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="14c38-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="14c38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c38-115">-DefaultProfile</span></span>
<span data-ttu-id="14c38-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="14c38-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14c38-117">-Name</span><span class="sxs-lookup"><span data-stu-id="14c38-117">-Name</span></span>
<span data-ttu-id="14c38-118">Gibt einen Namen für die Verbindung an, für die dieses Cmdlet ein Feld ändert.</span><span class="sxs-lookup"><span data-stu-id="14c38-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="14c38-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c38-119">-ResourceGroupName</span></span>
<span data-ttu-id="14c38-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Feld in einer Verbindung ändert.</span><span class="sxs-lookup"><span data-stu-id="14c38-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="14c38-121">-Value</span><span class="sxs-lookup"><span data-stu-id="14c38-121">-Value</span></span>
<span data-ttu-id="14c38-122">Gibt einen Wert an, der im Verbindungsfeld geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="14c38-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="14c38-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c38-123">CommonParameters</span></span>
<span data-ttu-id="14c38-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14c38-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c38-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c38-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c38-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14c38-126">INPUTS</span></span>

### <span data-ttu-id="14c38-127">System.String</span><span class="sxs-lookup"><span data-stu-id="14c38-127">System.String</span></span>

### <span data-ttu-id="14c38-128">System.Object</span><span class="sxs-lookup"><span data-stu-id="14c38-128">System.Object</span></span>

## <span data-ttu-id="14c38-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14c38-129">OUTPUTS</span></span>

### <span data-ttu-id="14c38-130">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="14c38-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="14c38-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="14c38-131">NOTES</span></span>

## <span data-ttu-id="14c38-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="14c38-132">RELATED LINKS</span></span>

[<span data-ttu-id="14c38-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="14c38-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


