---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f4d17fa6cdcb64aab2ab373420891f686facfdf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502261"
---
# <span data-ttu-id="e75ac-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e75ac-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="e75ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e75ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e75ac-103">Ruft eine Liste der Azure-Automatisierungs-Software Update Konfigurationen ab.</span><span class="sxs-lookup"><span data-stu-id="e75ac-103">Gets a list of azure automation software update configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e75ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e75ac-104">SYNTAX</span></span>

### <span data-ttu-id="e75ac-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="e75ac-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e75ac-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e75ac-106">ByName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e75ac-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="e75ac-107">ByVMId</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e75ac-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e75ac-108">DESCRIPTION</span></span>
<span data-ttu-id="e75ac-109">Die Get-AzureRmAutomationSoftwareUpdateConfiguration gibt eine Liste der Software Update Konfigurationen zurück.</span><span class="sxs-lookup"><span data-stu-id="e75ac-109">The Get-AzureRmAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="e75ac-110">Um eine bestimmte Software Update Konfiguration zu erhalten, geben Sie den Parameter Name an.</span><span class="sxs-lookup"><span data-stu-id="e75ac-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="e75ac-111">Sie können auch Software Update Konfigurationen auflisten, die auf bestimmte Azure Virtual Machine ausgerichtet sind, indem Sie die Azure-Ressourcen-ID für diesen virtuellen Computer angeben.</span><span class="sxs-lookup"><span data-stu-id="e75ac-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="e75ac-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e75ac-112">EXAMPLES</span></span>

### <span data-ttu-id="e75ac-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e75ac-113">Example 1</span></span>
<span data-ttu-id="e75ac-114">Erhalten Sie eine Azure Automation-Software Update Konfiguration nach Namen.</span><span class="sxs-lookup"><span data-stu-id="e75ac-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

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

## <span data-ttu-id="e75ac-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e75ac-115">PARAMETERS</span></span>

### <span data-ttu-id="e75ac-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e75ac-116">-AutomationAccountName</span></span>
<span data-ttu-id="e75ac-117">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="e75ac-117">The automation account name.</span></span>

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

### <span data-ttu-id="e75ac-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="e75ac-118">-AzureVMResourceId</span></span>
<span data-ttu-id="e75ac-119">Die Azure-Ressourcen-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="e75ac-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="e75ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e75ac-120">-DefaultProfile</span></span>
<span data-ttu-id="e75ac-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e75ac-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e75ac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e75ac-122">-Name</span></span>
<span data-ttu-id="e75ac-123">Der Name der Software Update Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e75ac-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="e75ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e75ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="e75ac-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e75ac-125">The resource group name.</span></span>

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

### <span data-ttu-id="e75ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e75ac-126">CommonParameters</span></span>
<span data-ttu-id="e75ac-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e75ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e75ac-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e75ac-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e75ac-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e75ac-129">INPUTS</span></span>

### <span data-ttu-id="e75ac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e75ac-130">System.String</span></span>

## <span data-ttu-id="e75ac-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e75ac-131">OUTPUTS</span></span>

### <span data-ttu-id="e75ac-132">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e75ac-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="e75ac-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e75ac-133">NOTES</span></span>

## <span data-ttu-id="e75ac-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e75ac-134">RELATED LINKS</span></span>
