---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 7426f49d94e82865163320fecd85704aeeff14b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499085"
---
# <span data-ttu-id="0353b-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0353b-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="0353b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0353b-102">SYNOPSIS</span></span>
<span data-ttu-id="0353b-103">Ändert eine Automatisierungs Variable.</span><span class="sxs-lookup"><span data-stu-id="0353b-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0353b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0353b-104">SYNTAX</span></span>

### <span data-ttu-id="0353b-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="0353b-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0353b-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="0353b-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0353b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0353b-107">DESCRIPTION</span></span>
<span data-ttu-id="0353b-108">Das Cmdlet " **Satz-AzureRmAutomationVariable** " ändert den Wert oder die Beschreibung einer Variablen in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="0353b-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="0353b-109">Um die Variable zu verschlüsseln, geben Sie den *verschlüsselten* Parameter an.</span><span class="sxs-lookup"><span data-stu-id="0353b-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="0353b-110">Der verschlüsselte Zustand einer Variablen kann nach der Erstellung nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0353b-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="0353b-111">Bei einer vorhandenen, nicht verschlüsselten Variablen wird eine *verschlüsselte* Variable angegeben.</span><span class="sxs-lookup"><span data-stu-id="0353b-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="0353b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0353b-112">EXAMPLES</span></span>

### <span data-ttu-id="0353b-113">Beispiel 1: Setzen des Werts einer Variablen</span><span class="sxs-lookup"><span data-stu-id="0353b-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="0353b-114">Mit diesem Befehl wird ein neuer Wert für die Variable mit dem Namen StringVariable22 im Azure-Automatisierungs Konto mit dem Namen Contoso17 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0353b-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="0353b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0353b-115">PARAMETERS</span></span>

### <span data-ttu-id="0353b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0353b-116">-AutomationAccountName</span></span>
<span data-ttu-id="0353b-117">Gibt den Namen des Automatisierungs Kontos an, in dem die Variable gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0353b-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0353b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0353b-118">-DefaultProfile</span></span>
<span data-ttu-id="0353b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0353b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0353b-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0353b-120">-Description</span></span>
<span data-ttu-id="0353b-121">Gibt eine Beschreibung für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="0353b-121">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0353b-122">-Verschlüsselt</span><span class="sxs-lookup"><span data-stu-id="0353b-122">-Encrypted</span></span>
<span data-ttu-id="0353b-123">Gibt an, ob das Cmdlet den Wert der Variablen für den Speicher verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="0353b-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0353b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0353b-124">-Name</span></span>
<span data-ttu-id="0353b-125">Gibt den Namen der Variablen an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0353b-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0353b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0353b-126">-ResourceGroupName</span></span>
<span data-ttu-id="0353b-127">Gibt die Ressourcengruppe an, für die mit diesem Cmdlet eine Variable geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0353b-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="0353b-128">-Wert</span><span class="sxs-lookup"><span data-stu-id="0353b-128">-Value</span></span>
<span data-ttu-id="0353b-129">Gibt einen Wert für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="0353b-129">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0353b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0353b-130">CommonParameters</span></span>
<span data-ttu-id="0353b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0353b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0353b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0353b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0353b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0353b-133">INPUTS</span></span>

### <span data-ttu-id="0353b-134">Keine</span><span class="sxs-lookup"><span data-stu-id="0353b-134">None</span></span>
<span data-ttu-id="0353b-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0353b-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0353b-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0353b-136">OUTPUTS</span></span>

### <span data-ttu-id="0353b-137">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="0353b-137">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="0353b-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="0353b-138">NOTES</span></span>

## <span data-ttu-id="0353b-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0353b-139">RELATED LINKS</span></span>

[<span data-ttu-id="0353b-140">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0353b-140">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="0353b-141">Neu – AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0353b-141">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="0353b-142">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0353b-142">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


