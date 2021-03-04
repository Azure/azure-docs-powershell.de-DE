---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b71da123933cd190038164b67d37fb81b0d5c973
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944777"
---
# <span data-ttu-id="7c8f0-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7c8f0-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="7c8f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8f0-103">Ruft die Einstellungsdatei für den Azure-Websitewiederherstellungstresor ab.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="7c8f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c8f0-104">SYNTAX</span></span>

### <span data-ttu-id="7c8f0-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="7c8f0-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c8f0-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="7c8f0-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c8f0-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="7c8f0-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c8f0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c8f0-108">DESCRIPTION</span></span>
<span data-ttu-id="7c8f0-109">Das **Get-AzRecoveryServicesVaultSettingsFile-Cmdlet** ruft die Einstellungsdatei für einen Azure-Websitewiederherstellungstresor ab.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7c8f0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c8f0-110">EXAMPLES</span></span>

### <span data-ttu-id="7c8f0-111">Beispiel 1: Registrieren eines Windows Server- oder DPM-Computers für Azure Backup</span><span class="sxs-lookup"><span data-stu-id="7c8f0-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="7c8f0-112">Der erste Befehl ruft den Tresor mit dem Namen TestVault ab und speichert ihn dann in der $Vault 01-Variable.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="7c8f0-113">Der zweite Befehl legt die $CredsPath auf C:\Downloads fest.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="7c8f0-114">Der letzte Befehl ruft die Tresoranmeldeinformationendatei für $Vault 01 ab, indem die Anmeldeinformationen in $CredsPath Azure Backup verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="7c8f0-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7c8f0-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="7c8f0-116">Der Befehl ruft die Datei mit den Tresoranmeldeinformationen für $Vault 01 des Tresortyps "siteRecovery" ab.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="7c8f0-117">Beispiel 3: Registrieren eines Windows Server- oder DPM-Computers für Azure Backup</span><span class="sxs-lookup"><span data-stu-id="7c8f0-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="7c8f0-118">Der Befehl ruft die Datei mit den Anmeldeinformationen des Tresors für $Vault 01 ab.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="7c8f0-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7c8f0-119">PARAMETERS</span></span>

### <span data-ttu-id="7c8f0-120">-Sicherung</span><span class="sxs-lookup"><span data-stu-id="7c8f0-120">-Backup</span></span>
<span data-ttu-id="7c8f0-121">Gibt an, dass die Datei mit den Anmeldeinformationen des Tresors für Azure Backup gilt.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f0-122">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="7c8f0-122">-Certificate</span></span>
<span data-ttu-id="7c8f0-123">{{Fill Certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="7c8f0-123">{{Fill Certificate Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8f0-124">-DefaultProfile</span></span>
<span data-ttu-id="7c8f0-125">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c8f0-126">-Path</span><span class="sxs-lookup"><span data-stu-id="7c8f0-126">-Path</span></span>
<span data-ttu-id="7c8f0-127">Gibt den Pfad zur Azure Site Recovery-Tresoreinstellungendatei an.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="7c8f0-128">Sie können diese Datei aus dem Azure Site Recovery-Tresorportal herunterladen und lokal speichern.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f0-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7c8f0-129">-SiteFriendlyName</span></span>
<span data-ttu-id="7c8f0-130">Gibt den websitefreundlichen Namen an.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="7c8f0-131">Verwenden Sie diesen Parameter, wenn Sie die Tresoranmeldeinformationen für eine Hyper-V-Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f0-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="7c8f0-132">-SiteIdentifier</span></span>
<span data-ttu-id="7c8f0-133">Gibt den Websitebezeichner an.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-133">Specifies the site identifier.</span></span>
<span data-ttu-id="7c8f0-134">Verwenden Sie diesen Parameter, wenn Sie die Tresoranmeldeinformationen für eine Hyper-V-Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f0-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7c8f0-135">-SiteRecovery</span></span>
<span data-ttu-id="7c8f0-136">Gibt an, dass die Datei mit den Anmeldeinformationen des Tresors für die Azure-Websitewiederherstellung gilt.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f0-137">-Vault</span><span class="sxs-lookup"><span data-stu-id="7c8f0-137">-Vault</span></span>
<span data-ttu-id="7c8f0-138">Gibt das Azure Site Recovery-Tresorobjekt an.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-138">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8f0-139">CommonParameters</span></span>
<span data-ttu-id="7c8f0-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8f0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8f0-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c8f0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8f0-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c8f0-142">INPUTS</span></span>

### <span data-ttu-id="7c8f0-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="7c8f0-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7c8f0-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c8f0-144">OUTPUTS</span></span>

### <span data-ttu-id="7c8f0-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="7c8f0-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="7c8f0-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7c8f0-146">NOTES</span></span>

## <span data-ttu-id="7c8f0-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7c8f0-147">RELATED LINKS</span></span>

[<span data-ttu-id="7c8f0-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7c8f0-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="7c8f0-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7c8f0-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="7c8f0-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7c8f0-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


