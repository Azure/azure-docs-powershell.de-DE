---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008709"
---
# <span data-ttu-id="0affb-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0affb-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="0affb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0affb-102">SYNOPSIS</span></span>
<span data-ttu-id="0affb-103">Ändert eine Automatisierungs Variable.</span><span class="sxs-lookup"><span data-stu-id="0affb-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="0affb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0affb-104">SYNTAX</span></span>

### <span data-ttu-id="0affb-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="0affb-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0affb-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="0affb-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0affb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0affb-107">DESCRIPTION</span></span>
<span data-ttu-id="0affb-108">Das Cmdlet " **Satz-AzAutomationVariable** " ändert den Wert oder die Beschreibung einer Variablen in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="0affb-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="0affb-109">Um die Variable zu verschlüsseln, geben Sie den *verschlüsselten* Parameter an.</span><span class="sxs-lookup"><span data-stu-id="0affb-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="0affb-110">Der verschlüsselte Zustand einer Variablen kann nach der Erstellung nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0affb-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="0affb-111">Bei einer vorhandenen, nicht verschlüsselten Variablen wird eine *verschlüsselte* Variable angegeben.</span><span class="sxs-lookup"><span data-stu-id="0affb-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="0affb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0affb-112">EXAMPLES</span></span>

### <span data-ttu-id="0affb-113">Beispiel 1: Setzen des Werts einer Variablen</span><span class="sxs-lookup"><span data-stu-id="0affb-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="0affb-114">Mit diesem Befehl wird ein neuer Wert für die Variable mit dem Namen StringVariable22 im Azure-Automatisierungs Konto mit dem Namen Contoso17 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0affb-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="0affb-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0affb-115">PARAMETERS</span></span>

### <span data-ttu-id="0affb-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0affb-116">-AutomationAccountName</span></span>
<span data-ttu-id="0affb-117">Gibt den Namen des Automatisierungs Kontos an, in dem die Variable gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0affb-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="0affb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0affb-118">-DefaultProfile</span></span>
<span data-ttu-id="0affb-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0affb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0affb-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0affb-120">-Description</span></span>
<span data-ttu-id="0affb-121">Gibt eine Beschreibung für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="0affb-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0affb-122">-Verschlüsselt</span><span class="sxs-lookup"><span data-stu-id="0affb-122">-Encrypted</span></span>
<span data-ttu-id="0affb-123">Gibt an, ob das Cmdlet den Wert der Variablen für den Speicher verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="0affb-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0affb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0affb-124">-Name</span></span>
<span data-ttu-id="0affb-125">Gibt den Namen der Variablen an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0affb-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0affb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0affb-126">-ResourceGroupName</span></span>
<span data-ttu-id="0affb-127">Gibt die Ressourcengruppe an, für die mit diesem Cmdlet eine Variable geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0affb-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="0affb-128">-Wert</span><span class="sxs-lookup"><span data-stu-id="0affb-128">-Value</span></span>
<span data-ttu-id="0affb-129">Gibt einen Wert für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="0affb-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0affb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0affb-130">CommonParameters</span></span>
<span data-ttu-id="0affb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0affb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0affb-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0affb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0affb-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0affb-133">INPUTS</span></span>

### <span data-ttu-id="0affb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0affb-134">System.String</span></span>

### <span data-ttu-id="0affb-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0affb-135">System.Boolean</span></span>

### <span data-ttu-id="0affb-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="0affb-136">System.Object</span></span>

## <span data-ttu-id="0affb-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0affb-137">OUTPUTS</span></span>

### <span data-ttu-id="0affb-138">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="0affb-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="0affb-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0affb-139">NOTES</span></span>

## <span data-ttu-id="0affb-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0affb-140">RELATED LINKS</span></span>

[<span data-ttu-id="0affb-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0affb-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="0affb-142">Neu – AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0affb-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="0affb-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0affb-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


