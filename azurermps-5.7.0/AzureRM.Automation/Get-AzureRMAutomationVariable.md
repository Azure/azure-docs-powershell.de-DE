---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 5fccd3f6aa193a3c2cacf39e6b72bccdf440b393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505846"
---
# <span data-ttu-id="ea8e9-101">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ea8e9-101">Get-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="ea8e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea8e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8e9-103">Ruft eine Automatisierungs Variable ab.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-103">Gets an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea8e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea8e9-104">SYNTAX</span></span>

### <span data-ttu-id="ea8e9-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea8e9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea8e9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ea8e9-106">ByName</span></span>
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea8e9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea8e9-107">DESCRIPTION</span></span>
<span data-ttu-id="ea8e9-108">Das Cmdlet " **Get-AzureRmAutomationVariable** " ruft mindestens eine Azure-Automatisierungs Variablen ab.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-108">The **Get-AzureRmAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="ea8e9-109">Um eine bestimmte Variable abzurufen, geben Sie Ihren Namen ein.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="ea8e9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea8e9-110">EXAMPLES</span></span>

### <span data-ttu-id="ea8e9-111">Beispiel 1: Abrufen einer Variablen</span><span class="sxs-lookup"><span data-stu-id="ea8e9-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="ea8e9-112">Der erste Befehl ruft eine Automatisierungs Variable mit dem Namen Variable06 im Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="ea8e9-113">Der Befehl speichert das Objekt in der $Variable Variablen.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-113">The command stores that object in the $Variable variable.</span></span>

<span data-ttu-id="ea8e9-114">Der zweite Befehl verwendet die standardmäßige Punktnotation, um auf die **value** -Eigenschaft von $Variable zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="ea8e9-115">Der Befehl speichert den Wert in der $Value Variablen.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="ea8e9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea8e9-116">PARAMETERS</span></span>

### <span data-ttu-id="ea8e9-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ea8e9-117">-AutomationAccountName</span></span>
<span data-ttu-id="ea8e9-118">Gibt den Namen des Automatisierungs Kontos an, das die vom Cmdlet abgerufenen Variablen enthält.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ea8e9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8e9-119">-DefaultProfile</span></span>
<span data-ttu-id="ea8e9-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ea8e9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea8e9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ea8e9-121">-Name</span></span>
<span data-ttu-id="ea8e9-122">Gibt den Namen einer Variablen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-122">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8e9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea8e9-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea8e9-124">Gibt die Ressourcengruppe an, für die dieses Cmdlet Variablen erhält.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="ea8e9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8e9-125">CommonParameters</span></span>
<span data-ttu-id="ea8e9-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8e9-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea8e9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8e9-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea8e9-128">INPUTS</span></span>

### <span data-ttu-id="ea8e9-129">Keine</span><span class="sxs-lookup"><span data-stu-id="ea8e9-129">None</span></span>
<span data-ttu-id="ea8e9-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ea8e9-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea8e9-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea8e9-131">OUTPUTS</span></span>

### <span data-ttu-id="ea8e9-132">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="ea8e9-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="ea8e9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea8e9-133">NOTES</span></span>

## <span data-ttu-id="ea8e9-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea8e9-134">RELATED LINKS</span></span>

[<span data-ttu-id="ea8e9-135">Neu – AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ea8e9-135">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="ea8e9-136">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ea8e9-136">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="ea8e9-137">Satz-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ea8e9-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


