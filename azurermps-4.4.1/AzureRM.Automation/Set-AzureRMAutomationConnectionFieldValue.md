---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: c3f889f45a90b127287821afb789eab2908faffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503281"
---
# <span data-ttu-id="5a123-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="5a123-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="5a123-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a123-102">SYNOPSIS</span></span>
<span data-ttu-id="5a123-103">Ändert den Wert eines Felds in einer Automatisierungs Verbindung.</span><span class="sxs-lookup"><span data-stu-id="5a123-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a123-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a123-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a123-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a123-105">DESCRIPTION</span></span>
<span data-ttu-id="5a123-106">Das Cmdlet " **Satz-AzureRmAutomationConnectionFieldValue** " ändert den Wert eines Felds in einer Verbindung in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="5a123-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="5a123-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a123-107">EXAMPLES</span></span>

### <span data-ttu-id="5a123-108">Beispiel 1: Ändern eines Feld Werts in einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="5a123-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="5a123-109">Dieser Befehl ändert die Abonnement-ID für die Azure-Verbindung mit dem Namen ContosoConnection im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="5a123-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="5a123-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a123-110">PARAMETERS</span></span>

### <span data-ttu-id="5a123-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5a123-111">-AutomationAccountName</span></span>
<span data-ttu-id="5a123-112">Gibt den Namen des Automatisierungs Kontos an, für das mit diesem Cmdlet ein Feld in einer Verbindung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5a123-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="5a123-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="5a123-113">-ConnectionFieldName</span></span>
<span data-ttu-id="5a123-114">Gibt einen Namen für das Feld an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5a123-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5a123-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5a123-115">-Name</span></span>
<span data-ttu-id="5a123-116">Gibt einen Namen für die Verbindung an, für die dieses Cmdlet ein Feld geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5a123-116">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="5a123-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a123-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a123-118">Gibt den Namen der Ressourcengruppe an, für die mit diesem Cmdlet ein Feld in einer Verbindung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5a123-118">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="5a123-119">-Wert</span><span class="sxs-lookup"><span data-stu-id="5a123-119">-Value</span></span>
<span data-ttu-id="5a123-120">Gibt einen Wert an, der im Verbindungsfeld geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a123-120">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="5a123-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a123-121">-DefaultProfile</span></span>
<span data-ttu-id="5a123-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a123-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a123-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a123-123">CommonParameters</span></span>
<span data-ttu-id="5a123-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a123-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a123-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a123-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a123-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a123-126">INPUTS</span></span>

## <span data-ttu-id="5a123-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a123-127">OUTPUTS</span></span>

### <span data-ttu-id="5a123-128">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="5a123-128">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="5a123-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a123-129">NOTES</span></span>

## <span data-ttu-id="5a123-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a123-130">RELATED LINKS</span></span>

[<span data-ttu-id="5a123-131">Neu – AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5a123-131">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


