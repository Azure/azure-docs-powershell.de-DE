---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997364"
---
# <span data-ttu-id="9e4a3-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e4a3-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="9e4a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4a3-103">Ruft eine Liste der Azure-Automatisierungs-Software Update Konfigurationen ab.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="9e4a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e4a3-104">SYNTAX</span></span>

### <span data-ttu-id="9e4a3-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e4a3-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e4a3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9e4a3-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e4a3-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="9e4a3-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e4a3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e4a3-108">DESCRIPTION</span></span>
<span data-ttu-id="9e4a3-109">Die Get-AzAutomationSoftwareUpdateConfiguration gibt eine Liste der Software Update Konfigurationen zurück.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="9e4a3-110">Um eine bestimmte Software Update Konfiguration zu erhalten, geben Sie den Parameter Name an.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="9e4a3-111">Sie können auch Software Update Konfigurationen auflisten, die auf bestimmte Azure Virtual Machine ausgerichtet sind, indem Sie die Azure-Ressourcen-ID für diesen virtuellen Computer angeben.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="9e4a3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e4a3-112">EXAMPLES</span></span>

### <span data-ttu-id="9e4a3-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e4a3-113">Example 1</span></span>
<span data-ttu-id="9e4a3-114">Erhalten Sie eine Azure Automation-Software Update Konfiguration nach Namen.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-114">Get an azure automation software update configuration by name.</span></span>

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

## <span data-ttu-id="9e4a3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e4a3-115">PARAMETERS</span></span>

### <span data-ttu-id="9e4a3-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e4a3-116">-AutomationAccountName</span></span>
<span data-ttu-id="9e4a3-117">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-117">The automation account name.</span></span>

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

### <span data-ttu-id="9e4a3-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="9e4a3-118">-AzureVMResourceId</span></span>
<span data-ttu-id="9e4a3-119">Die Azure-Ressourcen-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="9e4a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4a3-120">-DefaultProfile</span></span>
<span data-ttu-id="9e4a3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e4a3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9e4a3-122">-Name</span></span>
<span data-ttu-id="9e4a3-123">Der Name der Software Update Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="9e4a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e4a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e4a3-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-125">The resource group name.</span></span>

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

### <span data-ttu-id="9e4a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4a3-126">CommonParameters</span></span>
<span data-ttu-id="9e4a3-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e4a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4a3-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e4a3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4a3-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e4a3-129">INPUTS</span></span>

### <span data-ttu-id="9e4a3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9e4a3-130">System.String</span></span>

## <span data-ttu-id="9e4a3-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e4a3-131">OUTPUTS</span></span>

### <span data-ttu-id="9e4a3-132">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e4a3-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="9e4a3-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e4a3-133">NOTES</span></span>

## <span data-ttu-id="9e4a3-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e4a3-134">RELATED LINKS</span></span>
