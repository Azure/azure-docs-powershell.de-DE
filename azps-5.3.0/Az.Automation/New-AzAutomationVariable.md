---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: f60e254e9addf2e7052b010033d9c81ccc6a0a98
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471298"
---
# <span data-ttu-id="aa743-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="aa743-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="aa743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa743-102">SYNOPSIS</span></span>
<span data-ttu-id="aa743-103">Erstellt eine Automatisierungsvariable.</span><span class="sxs-lookup"><span data-stu-id="aa743-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="aa743-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa743-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa743-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa743-105">DESCRIPTION</span></span>
<span data-ttu-id="aa743-106">Das **Cmdlet "New-AzAutomationVariable"** erstellt eine Variable in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="aa743-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="aa743-107">Um die Variable zu verschlüsseln, geben Sie den Parameter *"Encrypted"* an.</span><span class="sxs-lookup"><span data-stu-id="aa743-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="aa743-108">Sie können den verschlüsselten Zustand einer Variablen nach der Erstellung nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="aa743-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="aa743-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa743-109">EXAMPLES</span></span>

### <span data-ttu-id="aa743-110">Beispiel 1: Erstellen einer Variablen mit einem einfachen Wert</span><span class="sxs-lookup"><span data-stu-id="aa743-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aa743-111">Mit diesem Befehl wird eine Variable namens "StringVariable22" mit einem Zeichenfolgenwert im Automatisierungskonto namens "Contoso17" erstellt.</span><span class="sxs-lookup"><span data-stu-id="aa743-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="aa743-112">Beispiel 2: Erstellen einer Variablen mit einem komplexen Wert</span><span class="sxs-lookup"><span data-stu-id="aa743-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aa743-113">Der erste Befehl ruft mithilfe des cmdlets "Get-AzVM" einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="aa743-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="aa743-114">Der Befehl speichert sie in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="aa743-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aa743-115">Der zweite Befehl erstellt eine Variable namens "ComplexVariable01" im Automatisierungskonto namens "Contoso17".</span><span class="sxs-lookup"><span data-stu-id="aa743-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="aa743-116">Dieser Befehl verwendet ein komplexes Objekt für seinen Wert, in diesem Fall den virtuellen Computer in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="aa743-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="aa743-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa743-117">PARAMETERS</span></span>

### <span data-ttu-id="aa743-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aa743-118">-AutomationAccountName</span></span>
<span data-ttu-id="aa743-119">Gibt den Namen des Automatisierungskontos an, in dem die Variable gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa743-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="aa743-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa743-120">-DefaultProfile</span></span>
<span data-ttu-id="aa743-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aa743-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa743-122">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa743-122">-Description</span></span>
<span data-ttu-id="aa743-123">Gibt eine Beschreibung für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="aa743-123">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa743-124">-Encrypted</span><span class="sxs-lookup"><span data-stu-id="aa743-124">-Encrypted</span></span>
<span data-ttu-id="aa743-125">Gibt an, ob mit diesem Cmdlet der Wert der Variablen für die Speicherung verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="aa743-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa743-126">-Name</span><span class="sxs-lookup"><span data-stu-id="aa743-126">-Name</span></span>
<span data-ttu-id="aa743-127">Gibt einen Namen für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="aa743-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="aa743-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa743-128">-ResourceGroupName</span></span>
<span data-ttu-id="aa743-129">Gibt die Ressourcengruppe an, für die dieses Cmdlet eine Variable erstellt.</span><span class="sxs-lookup"><span data-stu-id="aa743-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="aa743-130">-Value</span><span class="sxs-lookup"><span data-stu-id="aa743-130">-Value</span></span>
<span data-ttu-id="aa743-131">Gibt einen Wert für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="aa743-131">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa743-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa743-132">CommonParameters</span></span>
<span data-ttu-id="aa743-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa743-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa743-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa743-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa743-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa743-135">INPUTS</span></span>

### <span data-ttu-id="aa743-136">System.String</span><span class="sxs-lookup"><span data-stu-id="aa743-136">System.String</span></span>

### <span data-ttu-id="aa743-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa743-137">System.Boolean</span></span>

### <span data-ttu-id="aa743-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="aa743-138">System.Object</span></span>

## <span data-ttu-id="aa743-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa743-139">OUTPUTS</span></span>

### <span data-ttu-id="aa743-140">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="aa743-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="aa743-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aa743-141">NOTES</span></span>

## <span data-ttu-id="aa743-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aa743-142">RELATED LINKS</span></span>

[<span data-ttu-id="aa743-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="aa743-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="aa743-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="aa743-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="aa743-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="aa743-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


