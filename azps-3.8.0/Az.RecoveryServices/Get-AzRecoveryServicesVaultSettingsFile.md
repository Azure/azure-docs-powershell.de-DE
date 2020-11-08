---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: ac293211c332d8e99a592eedf96bbc179be99912
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004919"
---
# <span data-ttu-id="f999e-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f999e-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="f999e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f999e-102">SYNOPSIS</span></span>
<span data-ttu-id="f999e-103">Ruft die Azure Site Recovery Vault Settings-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="f999e-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="f999e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f999e-104">SYNTAX</span></span>

### <span data-ttu-id="f999e-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="f999e-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f999e-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="f999e-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f999e-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="f999e-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f999e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f999e-108">DESCRIPTION</span></span>
<span data-ttu-id="f999e-109">Das Cmdlet " **Get-AzRecoveryServicesVaultSettingsFile** " Ruft die Einstellungsdatei für ein Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="f999e-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f999e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f999e-110">EXAMPLES</span></span>

### <span data-ttu-id="f999e-111">Beispiel 1: Registrieren eines Windows-Servers oder DPM-Computers für Azure-Sicherung</span><span class="sxs-lookup"><span data-stu-id="f999e-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="f999e-112">Der erste Befehl ruft den Tresor mit dem Namen TestVault ab und speichert ihn dann in der Variablen $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="f999e-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="f999e-113">Mit dem zweiten Befehl wird die $CredsPath-Variable auf C:\Downloads. festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f999e-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="f999e-114">Der letzte Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 unter Verwendung der Anmeldeinformationen in $CredsPath für Azure-Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="f999e-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="f999e-115">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="f999e-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="f999e-116">Der Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 des Vault-Typs siteRecovery ab.</span><span class="sxs-lookup"><span data-stu-id="f999e-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="f999e-117">Beispiel 3: Registrieren eines Windows-Servers oder DPM-Computers für Azure-Sicherung</span><span class="sxs-lookup"><span data-stu-id="f999e-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="f999e-118">Der Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 ab.</span><span class="sxs-lookup"><span data-stu-id="f999e-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="f999e-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f999e-119">PARAMETERS</span></span>

### <span data-ttu-id="f999e-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="f999e-120">-Backup</span></span>
<span data-ttu-id="f999e-121">Gibt an, dass die Vault-Anmeldeinformationsdatei auf Azure Backup anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="f999e-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="f999e-122">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="f999e-122">-Certificate</span></span>
<span data-ttu-id="f999e-123">{{Fill Certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="f999e-123">{{Fill Certificate Description}}</span></span>

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

### <span data-ttu-id="f999e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f999e-124">-DefaultProfile</span></span>
<span data-ttu-id="f999e-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f999e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f999e-126">-Path</span><span class="sxs-lookup"><span data-stu-id="f999e-126">-Path</span></span>
<span data-ttu-id="f999e-127">Gibt den Pfad zur Azure Site Recovery Vault Settings-Datei an.</span><span class="sxs-lookup"><span data-stu-id="f999e-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="f999e-128">Sie können diese Datei vom Azure Site Recovery Vault-Portal herunterladen und lokal speichern.</span><span class="sxs-lookup"><span data-stu-id="f999e-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="f999e-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f999e-129">-SiteFriendlyName</span></span>
<span data-ttu-id="f999e-130">Gibt den Anzeigenamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="f999e-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="f999e-131">Verwenden Sie diesen Parameter, wenn Sie die Vault-Anmeldeinformationen für eine Hyper-V-Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="f999e-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="f999e-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="f999e-132">-SiteIdentifier</span></span>
<span data-ttu-id="f999e-133">Gibt die Website-ID an.</span><span class="sxs-lookup"><span data-stu-id="f999e-133">Specifies the site identifier.</span></span>
<span data-ttu-id="f999e-134">Verwenden Sie diesen Parameter, wenn Sie die Vault-Anmeldeinformationen für eine Hyper-V-Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="f999e-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="f999e-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f999e-135">-SiteRecovery</span></span>
<span data-ttu-id="f999e-136">Gibt an, dass die Vault-Anmeldeinformationsdatei auf Azure Site Recovery anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="f999e-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="f999e-137">-Vault</span><span class="sxs-lookup"><span data-stu-id="f999e-137">-Vault</span></span>
<span data-ttu-id="f999e-138">Gibt das Azure Site Recovery Vault-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f999e-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="f999e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f999e-139">CommonParameters</span></span>
<span data-ttu-id="f999e-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f999e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f999e-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f999e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f999e-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f999e-142">INPUTS</span></span>

### <span data-ttu-id="f999e-143">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="f999e-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f999e-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f999e-144">OUTPUTS</span></span>

### <span data-ttu-id="f999e-145">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="f999e-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="f999e-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f999e-146">NOTES</span></span>

## <span data-ttu-id="f999e-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f999e-147">RELATED LINKS</span></span>

[<span data-ttu-id="f999e-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f999e-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="f999e-149">Neu – AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f999e-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="f999e-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f999e-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


