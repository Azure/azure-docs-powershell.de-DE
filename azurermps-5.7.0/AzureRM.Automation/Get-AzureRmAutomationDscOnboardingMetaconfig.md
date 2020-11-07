---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 34dcb85de9520882b9202edd38ae2e44d1bcafee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664699"
---
# <span data-ttu-id="d34bd-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="d34bd-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="d34bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d34bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d34bd-103">Erstellt Meta-Configuration. MOF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="d34bd-103">Creates meta-configuration .mof files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d34bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d34bd-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d34bd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d34bd-105">DESCRIPTION</span></span>
<span data-ttu-id="d34bd-106">Das Cmdlet " **Get-AzureRmAutomationDscOnboardingMetaconfig** " erstellt APS-metakonfigurations-(Managed Object Format)-Dateien (MOF).</span><span class="sxs-lookup"><span data-stu-id="d34bd-106">The **Get-AzureRmAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="d34bd-107">Mit diesem Cmdlet wird für jeden von Ihnen angegebenen Computernamen eine MOF-Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="d34bd-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="d34bd-108">Das Cmdlet erstellt einen Ordner für die MOF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="d34bd-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="d34bd-109">Sie können das Set-DscLocalConfigurationManager-Cmdlet für diesen Ordner ausführen, um diese Computer als DSC-Knoten in ein Azure Automation-Konto einzuführen.</span><span class="sxs-lookup"><span data-stu-id="d34bd-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="d34bd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d34bd-110">EXAMPLES</span></span>

### <span data-ttu-id="d34bd-111">Beispiel 1: Onboard-Server für Automatisierungs-DSC</span><span class="sxs-lookup"><span data-stu-id="d34bd-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="d34bd-112">Der erste Befehl erstellt DSC-metakonfigurations Dateien für zwei Server für das Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d34bd-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="d34bd-113">Der Befehl speichert diese Dateien auf einem Desktop.</span><span class="sxs-lookup"><span data-stu-id="d34bd-113">The command saves these files on a desktop.</span></span>

<span data-ttu-id="d34bd-114">Der zweite Befehl verwendet das Cmdlet " **DscLocalConfigurationManager** ", um die Meta-Konfiguration auf die angegebenen Computer anzuwenden, um Sie als DSC-Knoten an Bord zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="d34bd-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="d34bd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d34bd-115">PARAMETERS</span></span>

### <span data-ttu-id="d34bd-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d34bd-116">-AutomationAccountName</span></span>
<span data-ttu-id="d34bd-117">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d34bd-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="d34bd-118">Sie können an Bord der Computer, die der Parameter *Computername* für das Konto angibt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d34bd-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="d34bd-119">-Computername</span><span class="sxs-lookup"><span data-stu-id="d34bd-119">-ComputerName</span></span>
<span data-ttu-id="d34bd-120">Gibt ein Array von Namen von Computern an, für die dieses Cmdlet MOF-Dateien generiert.</span><span class="sxs-lookup"><span data-stu-id="d34bd-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="d34bd-121">Wenn Sie diesen Parameter nicht angeben, generiert das Cmdlet eine MOF-Datei für den aktuellen Computer (localhost).</span><span class="sxs-lookup"><span data-stu-id="d34bd-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34bd-122">-DefaultProfile</span></span>
<span data-ttu-id="d34bd-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d34bd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d34bd-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d34bd-124">-Force</span></span>
<span data-ttu-id="d34bd-125">Erzwingt, dass der Befehl ausgeführt wird, ohne dass Sie zur Bestätigung aufgefordert werden, und um vorhandene MOF-Dateien mit demselben Namen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d34bd-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34bd-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="d34bd-126">-OutputFolder</span></span>
<span data-ttu-id="d34bd-127">Gibt den Namen eines Ordners an, in dem das Cmdlet MOF-Dateien speichert.</span><span class="sxs-lookup"><span data-stu-id="d34bd-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34bd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34bd-128">-ResourceGroupName</span></span>
<span data-ttu-id="d34bd-129">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d34bd-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d34bd-130">Dieses Cmdlet erstellt MOF-Dateien für Onboard-Computer in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d34bd-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d34bd-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d34bd-131">-Confirm</span></span>
<span data-ttu-id="d34bd-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d34bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d34bd-133">-WhatIf</span></span>
<span data-ttu-id="d34bd-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d34bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d34bd-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d34bd-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34bd-136">CommonParameters</span></span>
<span data-ttu-id="d34bd-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34bd-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d34bd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34bd-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d34bd-139">INPUTS</span></span>

### <span data-ttu-id="d34bd-140">Keine</span><span class="sxs-lookup"><span data-stu-id="d34bd-140">None</span></span>
<span data-ttu-id="d34bd-141">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d34bd-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d34bd-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d34bd-142">OUTPUTS</span></span>

### <span data-ttu-id="d34bd-143">Microsoft. Azure. Commands. Automation. Model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="d34bd-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="d34bd-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d34bd-144">NOTES</span></span>

## <span data-ttu-id="d34bd-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d34bd-145">RELATED LINKS</span></span>

