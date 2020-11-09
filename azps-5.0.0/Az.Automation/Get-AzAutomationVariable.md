---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299823"
---
# <span data-ttu-id="86e23-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="86e23-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="86e23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86e23-102">SYNOPSIS</span></span>
<span data-ttu-id="86e23-103">Ruft eine Automatisierungs Variable ab.</span><span class="sxs-lookup"><span data-stu-id="86e23-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="86e23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86e23-104">SYNTAX</span></span>

### <span data-ttu-id="86e23-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="86e23-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86e23-106">ByName</span><span class="sxs-lookup"><span data-stu-id="86e23-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86e23-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86e23-107">DESCRIPTION</span></span>
<span data-ttu-id="86e23-108">Das Cmdlet " **Get-AzAutomationVariable** " ruft mindestens eine Azure-Automatisierungs Variablen ab.</span><span class="sxs-lookup"><span data-stu-id="86e23-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="86e23-109">Um eine bestimmte Variable abzurufen, geben Sie Ihren Namen ein.</span><span class="sxs-lookup"><span data-stu-id="86e23-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="86e23-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86e23-110">EXAMPLES</span></span>

### <span data-ttu-id="86e23-111">Beispiel 1: Abrufen einer Variablen</span><span class="sxs-lookup"><span data-stu-id="86e23-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="86e23-112">Der erste Befehl ruft eine Automatisierungs Variable mit dem Namen Variable06 im Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="86e23-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="86e23-113">Der Befehl speichert das Objekt in der $Variable Variablen.</span><span class="sxs-lookup"><span data-stu-id="86e23-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="86e23-114">Der zweite Befehl verwendet die standardmäßige Punktnotation, um auf die **value** -Eigenschaft von $Variable zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="86e23-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="86e23-115">Der Befehl speichert den Wert in der $Value Variablen.</span><span class="sxs-lookup"><span data-stu-id="86e23-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="86e23-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="86e23-116">PARAMETERS</span></span>

### <span data-ttu-id="86e23-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="86e23-117">-AutomationAccountName</span></span>
<span data-ttu-id="86e23-118">Gibt den Namen des Automatisierungs Kontos an, das die vom Cmdlet abgerufenen Variablen enthält.</span><span class="sxs-lookup"><span data-stu-id="86e23-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="86e23-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e23-119">-DefaultProfile</span></span>
<span data-ttu-id="86e23-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="86e23-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86e23-121">-Name</span><span class="sxs-lookup"><span data-stu-id="86e23-121">-Name</span></span>
<span data-ttu-id="86e23-122">Gibt den Namen einer Variablen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="86e23-122">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86e23-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e23-123">-ResourceGroupName</span></span>
<span data-ttu-id="86e23-124">Gibt die Ressourcengruppe an, für die dieses Cmdlet Variablen erhält.</span><span class="sxs-lookup"><span data-stu-id="86e23-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="86e23-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e23-125">CommonParameters</span></span>
<span data-ttu-id="86e23-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e23-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e23-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86e23-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e23-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86e23-128">INPUTS</span></span>

### <span data-ttu-id="86e23-129">System. String</span><span class="sxs-lookup"><span data-stu-id="86e23-129">System.String</span></span>

## <span data-ttu-id="86e23-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86e23-130">OUTPUTS</span></span>

### <span data-ttu-id="86e23-131">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="86e23-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="86e23-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="86e23-132">NOTES</span></span>

## <span data-ttu-id="86e23-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86e23-133">RELATED LINKS</span></span>

[<span data-ttu-id="86e23-134">Neu – AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="86e23-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="86e23-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="86e23-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="86e23-136">Satz-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="86e23-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


