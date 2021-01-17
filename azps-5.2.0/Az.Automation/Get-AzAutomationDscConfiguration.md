---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370473"
---
# <span data-ttu-id="eaa58-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="eaa58-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="eaa58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaa58-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa58-103">Ruft die DSC-Konfigurationen aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="eaa58-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="eaa58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eaa58-104">SYNTAX</span></span>

### <span data-ttu-id="eaa58-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="eaa58-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaa58-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="eaa58-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaa58-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eaa58-107">DESCRIPTION</span></span>
<span data-ttu-id="eaa58-108">Das **Cmdlet "Get-AzAutomationDscConfiguration"** ruft APS Desired State Configuration (DSC)-Konfigurationen aus der Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="eaa58-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="eaa58-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eaa58-109">EXAMPLES</span></span>

### <span data-ttu-id="eaa58-110">Beispiel 1: Alle -DSC-Konfigurationen erhalten</span><span class="sxs-lookup"><span data-stu-id="eaa58-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="eaa58-111">Dieser Befehl ruft Metadaten für alle DSC-Konfigurationen im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="eaa58-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="eaa58-112">Beispiel 2: Erhalten einer DSC-Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="eaa58-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="eaa58-113">Mit diesem Befehl werden Metadaten für eine DSC-Konfiguration namens "MyConfiguration" im Automatisierungskonto namens "Contoso17" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="eaa58-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="eaa58-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaa58-114">PARAMETERS</span></span>

### <span data-ttu-id="eaa58-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eaa58-115">-AutomationAccountName</span></span>
<span data-ttu-id="eaa58-116">Gibt den Namen des Automatisierungskontos an, das die VON diesem Cmdlet abgerufenen DSC-Konfigurationen enthält.</span><span class="sxs-lookup"><span data-stu-id="eaa58-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eaa58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa58-117">-DefaultProfile</span></span>
<span data-ttu-id="eaa58-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="eaa58-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaa58-119">-Name</span><span class="sxs-lookup"><span data-stu-id="eaa58-119">-Name</span></span>
<span data-ttu-id="eaa58-120">Gibt den Namen der DSC-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="eaa58-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa58-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaa58-121">-ResourceGroupName</span></span>
<span data-ttu-id="eaa58-122">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet DIE -DSC-Konfigurationen erhält.</span><span class="sxs-lookup"><span data-stu-id="eaa58-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="eaa58-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa58-123">CommonParameters</span></span>
<span data-ttu-id="eaa58-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaa58-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa58-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa58-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa58-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eaa58-126">INPUTS</span></span>

### <span data-ttu-id="eaa58-127">System.String</span><span class="sxs-lookup"><span data-stu-id="eaa58-127">System.String</span></span>

## <span data-ttu-id="eaa58-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eaa58-128">OUTPUTS</span></span>

### <span data-ttu-id="eaa58-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="eaa58-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="eaa58-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eaa58-130">NOTES</span></span>

## <span data-ttu-id="eaa58-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eaa58-131">RELATED LINKS</span></span>

[<span data-ttu-id="eaa58-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="eaa58-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="eaa58-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="eaa58-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


