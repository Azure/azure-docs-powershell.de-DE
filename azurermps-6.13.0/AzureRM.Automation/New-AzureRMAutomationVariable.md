---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: 4036261cd333194a71d302e57e97a1f017554da0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476294"
---
# <span data-ttu-id="a7294-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a7294-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="a7294-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7294-102">SYNOPSIS</span></span>
<span data-ttu-id="a7294-103">Erstellt eine Automatisierungs Variable.</span><span class="sxs-lookup"><span data-stu-id="a7294-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7294-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7294-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7294-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7294-105">DESCRIPTION</span></span>
<span data-ttu-id="a7294-106">Das Cmdlet **New-AzureRmAutomationVariable** erstellt eine Variable in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="a7294-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="a7294-107">Um die Variable zu verschlüsseln, geben Sie den *verschlüsselten* Parameter an.</span><span class="sxs-lookup"><span data-stu-id="a7294-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="a7294-108">Der verschlüsselte Zustand einer Variablen kann nach der Erstellung nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a7294-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="a7294-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7294-109">EXAMPLES</span></span>

### <span data-ttu-id="a7294-110">Beispiel 1: Erstellen einer Variablen mit einem einfachen Wert</span><span class="sxs-lookup"><span data-stu-id="a7294-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a7294-111">Dieser Befehl erstellt eine Variable mit dem Namen StringVariable22 mit einem Zeichenfolgenwert im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a7294-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a7294-112">Beispiel 2: Erstellen einer Variablen mit einem komplexen Wert</span><span class="sxs-lookup"><span data-stu-id="a7294-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a7294-113">Der erste Befehl ruft einen virtuellen Computer mithilfe des Get-AzureVM-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="a7294-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="a7294-114">Der Befehl speichert Sie in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a7294-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a7294-115">Der zweite Befehl erstellt eine Variable mit dem Namen ComplexVariable01 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a7294-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="a7294-116">Dieser Befehl verwendet ein komplexes Objekt für seinen Wert, in diesem Fall den virtuellen Computer in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a7294-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="a7294-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7294-117">PARAMETERS</span></span>

### <span data-ttu-id="a7294-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a7294-118">-AutomationAccountName</span></span>
<span data-ttu-id="a7294-119">Gibt den Namen des Automatisierungs Kontos an, in dem die Variable gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7294-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="a7294-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7294-120">-DefaultProfile</span></span>
<span data-ttu-id="a7294-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a7294-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7294-122">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7294-122">-Description</span></span>
<span data-ttu-id="a7294-123">Gibt eine Beschreibung für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="a7294-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="a7294-124">-Verschlüsselt</span><span class="sxs-lookup"><span data-stu-id="a7294-124">-Encrypted</span></span>
<span data-ttu-id="a7294-125">Gibt an, ob dieses Cmdlet den Wert der Variablen für den Speicher verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="a7294-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="a7294-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a7294-126">-Name</span></span>
<span data-ttu-id="a7294-127">Gibt einen Namen für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="a7294-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="a7294-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7294-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7294-129">Gibt die Ressourcengruppe an, für die mit diesem Cmdlet eine Variable erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a7294-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="a7294-130">-Wert</span><span class="sxs-lookup"><span data-stu-id="a7294-130">-Value</span></span>
<span data-ttu-id="a7294-131">Gibt einen Wert für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="a7294-131">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="a7294-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7294-132">CommonParameters</span></span>
<span data-ttu-id="a7294-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7294-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7294-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7294-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7294-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7294-135">INPUTS</span></span>

### <span data-ttu-id="a7294-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a7294-136">System.String</span></span>

### <span data-ttu-id="a7294-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7294-137">System.Boolean</span></span>

### <span data-ttu-id="a7294-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="a7294-138">System.Object</span></span>

## <span data-ttu-id="a7294-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7294-139">OUTPUTS</span></span>

### <span data-ttu-id="a7294-140">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="a7294-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="a7294-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7294-141">NOTES</span></span>

## <span data-ttu-id="a7294-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7294-142">RELATED LINKS</span></span>

[<span data-ttu-id="a7294-143">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a7294-143">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="a7294-144">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a7294-144">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="a7294-145">Satz-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a7294-145">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


