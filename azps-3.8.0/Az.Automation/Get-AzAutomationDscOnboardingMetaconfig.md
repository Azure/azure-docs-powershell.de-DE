---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 007142cb854e2e428983f95d7bb7397c5a0ace39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997397"
---
# <span data-ttu-id="ed5e6-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="ed5e6-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="ed5e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5e6-103">Erstellt Meta-Configuration. MOF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="ed5e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed5e6-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed5e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed5e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ed5e6-106">Das Cmdlet " **Get-AzAutomationDscOnboardingMetaconfig** " erstellt APS-metakonfigurations-(Managed Object Format)-Dateien (MOF).</span><span class="sxs-lookup"><span data-stu-id="ed5e6-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="ed5e6-107">Mit diesem Cmdlet wird für jeden von Ihnen angegebenen Computernamen eine MOF-Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="ed5e6-108">Das Cmdlet erstellt einen Ordner für die MOF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="ed5e6-109">Sie können das Set-DscLocalConfigurationManager-Cmdlet für diesen Ordner ausführen, um diese Computer als DSC-Knoten in ein Azure Automation-Konto einzuführen.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="ed5e6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed5e6-110">EXAMPLES</span></span>

### <span data-ttu-id="ed5e6-111">Beispiel 1: Onboard-Server für Automatisierungs-DSC</span><span class="sxs-lookup"><span data-stu-id="ed5e6-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="ed5e6-112">Der erste Befehl erstellt DSC-metakonfigurations Dateien für zwei Server für das Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="ed5e6-113">Der Befehl speichert diese Dateien auf einem Desktop.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="ed5e6-114">Der zweite Befehl verwendet das Cmdlet " **DscLocalConfigurationManager** ", um die Meta-Konfiguration auf die angegebenen Computer anzuwenden, um Sie als DSC-Knoten an Bord zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="ed5e6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed5e6-115">PARAMETERS</span></span>

### <span data-ttu-id="ed5e6-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed5e6-116">-AutomationAccountName</span></span>
<span data-ttu-id="ed5e6-117">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="ed5e6-118">Sie können an Bord der Computer, die der Parameter *Computername* für das Konto angibt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed5e6-119">-Computername</span><span class="sxs-lookup"><span data-stu-id="ed5e6-119">-ComputerName</span></span>
<span data-ttu-id="ed5e6-120">Gibt ein Array von Namen von Computern an, für die dieses Cmdlet MOF-Dateien generiert.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="ed5e6-121">Wenn Sie diesen Parameter nicht angeben, generiert das Cmdlet eine MOF-Datei für den aktuellen Computer (localhost).</span><span class="sxs-lookup"><span data-stu-id="ed5e6-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5e6-122">-DefaultProfile</span></span>
<span data-ttu-id="ed5e6-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ed5e6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed5e6-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ed5e6-124">-Force</span></span>
<span data-ttu-id="ed5e6-125">Erzwingt, dass der Befehl ausgeführt wird, ohne dass Sie zur Bestätigung aufgefordert werden, und um vorhandene MOF-Dateien mit demselben Namen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e6-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="ed5e6-126">-OutputFolder</span></span>
<span data-ttu-id="ed5e6-127">Gibt den Namen eines Ordners an, in dem das Cmdlet MOF-Dateien speichert.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="ed5e6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5e6-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed5e6-129">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ed5e6-130">Dieses Cmdlet erstellt MOF-Dateien für Onboard-Computer in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed5e6-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed5e6-131">-Confirm</span></span>
<span data-ttu-id="ed5e6-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5e6-133">-WhatIf</span></span>
<span data-ttu-id="ed5e6-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed5e6-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5e6-136">CommonParameters</span></span>
<span data-ttu-id="ed5e6-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5e6-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed5e6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5e6-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed5e6-139">INPUTS</span></span>

### <span data-ttu-id="ed5e6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ed5e6-140">System.String</span></span>

### <span data-ttu-id="ed5e6-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="ed5e6-141">System.String[]</span></span>

## <span data-ttu-id="ed5e6-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed5e6-142">OUTPUTS</span></span>

### <span data-ttu-id="ed5e6-143">Microsoft. Azure. Commands. Automation. Model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="ed5e6-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="ed5e6-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed5e6-144">NOTES</span></span>

## <span data-ttu-id="ed5e6-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed5e6-145">RELATED LINKS</span></span>
