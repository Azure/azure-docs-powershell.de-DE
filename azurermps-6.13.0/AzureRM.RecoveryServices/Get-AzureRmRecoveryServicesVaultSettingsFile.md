---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: a0572e73d270a37b3c705018a38b4a88fe88d1e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503434"
---
# <span data-ttu-id="31282-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="31282-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="31282-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31282-102">SYNOPSIS</span></span>
<span data-ttu-id="31282-103">Ruft die Azure Site Recovery Vault Settings-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="31282-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31282-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31282-104">SYNTAX</span></span>

### <span data-ttu-id="31282-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="31282-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31282-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="31282-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31282-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="31282-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31282-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31282-108">DESCRIPTION</span></span>
<span data-ttu-id="31282-109">Das Cmdlet " **Get-AzureRmRecoveryServicesVaultSettingsFile** " Ruft die Einstellungsdatei für ein Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="31282-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="31282-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31282-110">EXAMPLES</span></span>

### <span data-ttu-id="31282-111">Beispiel 1: Registrieren eines Windows-Servers oder DPM-Computers für Azure-Sicherung</span><span class="sxs-lookup"><span data-stu-id="31282-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="31282-112">Der erste Befehl ruft den Tresor mit dem Namen TestVault ab und speichert ihn dann in der Variablen $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="31282-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="31282-113">Mit dem zweiten Befehl wird die $CredsPath-Variable auf C:\Downloads. festgelegt.</span><span class="sxs-lookup"><span data-stu-id="31282-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="31282-114">Der letzte Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 unter Verwendung der Anmeldeinformationen in $CredsPath für Azure-Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="31282-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="31282-115">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="31282-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="31282-116">Der Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 des Vault-Typs siteRecovery ab.</span><span class="sxs-lookup"><span data-stu-id="31282-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="31282-117">Beispiel 3: Registrieren eines Windows-Servers oder DPM-Computers für Azure-Sicherung</span><span class="sxs-lookup"><span data-stu-id="31282-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="31282-118">Der Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 ab.</span><span class="sxs-lookup"><span data-stu-id="31282-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="31282-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="31282-119">PARAMETERS</span></span>

### <span data-ttu-id="31282-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="31282-120">-Backup</span></span>
<span data-ttu-id="31282-121">Gibt an, dass die Vault-Anmeldeinformationsdatei auf Azure Backup anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="31282-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31282-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31282-122">-DefaultProfile</span></span>
<span data-ttu-id="31282-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31282-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31282-124">-Path</span><span class="sxs-lookup"><span data-stu-id="31282-124">-Path</span></span>
<span data-ttu-id="31282-125">Gibt den Pfad zur Azure Site Recovery Vault Settings-Datei an.</span><span class="sxs-lookup"><span data-stu-id="31282-125">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="31282-126">Sie können diese Datei vom Azure Site Recovery Vault-Portal herunterladen und lokal speichern.</span><span class="sxs-lookup"><span data-stu-id="31282-126">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="31282-127">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="31282-127">-SiteFriendlyName</span></span>
<span data-ttu-id="31282-128">Gibt den Anzeigenamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="31282-128">Specifies the site friendly name.</span></span>
<span data-ttu-id="31282-129">Verwenden Sie diesen Parameter, wenn Sie die Vault-Anmeldeinformationen für eine Hyper-V-Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="31282-129">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31282-130">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="31282-130">-SiteIdentifier</span></span>
<span data-ttu-id="31282-131">Gibt die Website-ID an.</span><span class="sxs-lookup"><span data-stu-id="31282-131">Specifies the site identifier.</span></span>
<span data-ttu-id="31282-132">Verwenden Sie diesen Parameter, wenn Sie die Vault-Anmeldeinformationen für eine Hyper-V-Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="31282-132">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31282-133">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="31282-133">-SiteRecovery</span></span>
<span data-ttu-id="31282-134">Gibt an, dass die Vault-Anmeldeinformationsdatei auf Azure Site Recovery anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="31282-134">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31282-135">-Vault</span><span class="sxs-lookup"><span data-stu-id="31282-135">-Vault</span></span>
<span data-ttu-id="31282-136">Gibt das Azure Site Recovery Vault-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="31282-136">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="31282-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31282-137">CommonParameters</span></span>
<span data-ttu-id="31282-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31282-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31282-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31282-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31282-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31282-140">INPUTS</span></span>

### <span data-ttu-id="31282-141">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="31282-141">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="31282-142">Parameter: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="31282-142">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="31282-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31282-143">OUTPUTS</span></span>

### <span data-ttu-id="31282-144">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="31282-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="31282-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="31282-145">NOTES</span></span>

## <span data-ttu-id="31282-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31282-146">RELATED LINKS</span></span>

[<span data-ttu-id="31282-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="31282-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="31282-148">Neu – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="31282-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="31282-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="31282-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


