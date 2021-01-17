---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373734"
---
# <span data-ttu-id="c5a35-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5a35-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="c5a35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5a35-102">SYNOPSIS</span></span>
<span data-ttu-id="c5a35-103">Ruft eine Liste der Updatekonfigurationen für Azure-Automatisierungssoftware ab.</span><span class="sxs-lookup"><span data-stu-id="c5a35-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="c5a35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5a35-104">SYNTAX</span></span>

### <span data-ttu-id="c5a35-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5a35-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5a35-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c5a35-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5a35-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="c5a35-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5a35-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5a35-108">DESCRIPTION</span></span>
<span data-ttu-id="c5a35-109">Die Get-AzAutomationSoftwareUpdateConfiguration gibt eine Liste der Softwareupdatekonfigurationen zurück.</span><span class="sxs-lookup"><span data-stu-id="c5a35-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="c5a35-110">Um eine bestimmte Softwareupdatekonfiguration zu erhalten, geben Sie den Namensparameter an.</span><span class="sxs-lookup"><span data-stu-id="c5a35-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="c5a35-111">Sie können auch Softwareupdatekonfigurationen für einen bestimmten virtuellen Azure-Computer auflisten, indem Sie die Azure-Ressourcen-ID für diesen virtuellen Computer angeben.</span><span class="sxs-lookup"><span data-stu-id="c5a35-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="c5a35-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c5a35-112">EXAMPLES</span></span>

### <span data-ttu-id="c5a35-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5a35-113">Example 1</span></span>
<span data-ttu-id="c5a35-114">Holen Sie sich eine Updatekonfiguration für die Azure-Automatisierungssoftware nach Name.</span><span class="sxs-lookup"><span data-stu-id="c5a35-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Succeeded
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:37 AM +00:00
Description           :
```

## <span data-ttu-id="c5a35-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5a35-115">PARAMETERS</span></span>

### <span data-ttu-id="c5a35-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c5a35-116">-AutomationAccountName</span></span>
<span data-ttu-id="c5a35-117">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="c5a35-117">The automation account name.</span></span>

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

### <span data-ttu-id="c5a35-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="c5a35-118">-AzureVMResourceId</span></span>
<span data-ttu-id="c5a35-119">Azure-Ressourcen-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c5a35-119">Azure resource Id of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVMId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5a35-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5a35-120">-DefaultProfile</span></span>
<span data-ttu-id="c5a35-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5a35-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5a35-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c5a35-122">-Name</span></span>
<span data-ttu-id="c5a35-123">Name der Softwareupdatekonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c5a35-123">Name of the software update configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5a35-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5a35-124">-ResourceGroupName</span></span>
<span data-ttu-id="c5a35-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c5a35-125">The resource group name.</span></span>

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

### <span data-ttu-id="c5a35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5a35-126">CommonParameters</span></span>
<span data-ttu-id="c5a35-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5a35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5a35-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5a35-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5a35-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c5a35-129">INPUTS</span></span>

### <span data-ttu-id="c5a35-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c5a35-130">System.String</span></span>

## <span data-ttu-id="c5a35-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c5a35-131">OUTPUTS</span></span>

### <span data-ttu-id="c5a35-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5a35-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="c5a35-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c5a35-133">NOTES</span></span>

## <span data-ttu-id="c5a35-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c5a35-134">RELATED LINKS</span></span>
