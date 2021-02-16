---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 2df58153b2617a8ad62b0e46544128fa47a462b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149377"
---
# <span data-ttu-id="af8be-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="af8be-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="af8be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af8be-102">SYNOPSIS</span></span>
<span data-ttu-id="af8be-103">Ändert den Wert eines Felds in einer Automatisierungsverbindung.</span><span class="sxs-lookup"><span data-stu-id="af8be-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="af8be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af8be-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af8be-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af8be-105">DESCRIPTION</span></span>
<span data-ttu-id="af8be-106">Das **Cmdlet "Set-AzAutomationConnectionFieldValue"** ändert den Wert eines Felds in einer Verbindung in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="af8be-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="af8be-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af8be-107">EXAMPLES</span></span>

### <span data-ttu-id="af8be-108">Beispiel 1: Ändern eines Feldwerts in einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="af8be-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="af8be-109">Mit diesem Befehl wird die Abonnement-ID für die Azure-Verbindung namens "ContosoConnection" im Automatisierungskonto namens "AutomationAccount01" geändert.</span><span class="sxs-lookup"><span data-stu-id="af8be-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="af8be-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af8be-110">PARAMETERS</span></span>

### <span data-ttu-id="af8be-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="af8be-111">-AutomationAccountName</span></span>
<span data-ttu-id="af8be-112">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet ein Feld in einer Verbindung ändert.</span><span class="sxs-lookup"><span data-stu-id="af8be-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="af8be-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="af8be-113">-ConnectionFieldName</span></span>
<span data-ttu-id="af8be-114">Gibt einen Namen für das Feld an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="af8be-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="af8be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af8be-115">-DefaultProfile</span></span>
<span data-ttu-id="af8be-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="af8be-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af8be-117">-Name</span><span class="sxs-lookup"><span data-stu-id="af8be-117">-Name</span></span>
<span data-ttu-id="af8be-118">Gibt einen Namen für die Verbindung an, für die dieses Cmdlet ein Feld ändert.</span><span class="sxs-lookup"><span data-stu-id="af8be-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="af8be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af8be-119">-ResourceGroupName</span></span>
<span data-ttu-id="af8be-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Feld in einer Verbindung ändert.</span><span class="sxs-lookup"><span data-stu-id="af8be-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="af8be-121">-Value</span><span class="sxs-lookup"><span data-stu-id="af8be-121">-Value</span></span>
<span data-ttu-id="af8be-122">Gibt einen Wert an, der im Verbindungsfeld geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="af8be-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="af8be-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af8be-123">CommonParameters</span></span>
<span data-ttu-id="af8be-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af8be-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af8be-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af8be-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af8be-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af8be-126">INPUTS</span></span>

### <span data-ttu-id="af8be-127">System.String</span><span class="sxs-lookup"><span data-stu-id="af8be-127">System.String</span></span>

### <span data-ttu-id="af8be-128">System.Object</span><span class="sxs-lookup"><span data-stu-id="af8be-128">System.Object</span></span>

## <span data-ttu-id="af8be-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af8be-129">OUTPUTS</span></span>

### <span data-ttu-id="af8be-130">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="af8be-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="af8be-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="af8be-131">NOTES</span></span>

## <span data-ttu-id="af8be-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="af8be-132">RELATED LINKS</span></span>

[<span data-ttu-id="af8be-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="af8be-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


