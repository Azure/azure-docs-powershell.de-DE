---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b272f22c0bac37f5318deff50f1f0b56a849ce2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663764"
---
# <span data-ttu-id="2eb0d-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2eb0d-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="2eb0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2eb0d-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb0d-103">Ruft die Azure Site Recovery Vault Settings-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eb0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eb0d-104">SYNTAX</span></span>

### <span data-ttu-id="2eb0d-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="2eb0d-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2eb0d-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="2eb0d-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb0d-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="2eb0d-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eb0d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2eb0d-108">DESCRIPTION</span></span>
<span data-ttu-id="2eb0d-109">Das Cmdlet " **Get-AzureRmRecoveryServicesVaultSettingsFile** " Ruft die Einstellungsdatei für ein Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="2eb0d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2eb0d-110">EXAMPLES</span></span>

### <span data-ttu-id="2eb0d-111">Beispiel 1: Registrieren eines Windows-Servers oder DPM-Computers für Azure-Sicherung</span><span class="sxs-lookup"><span data-stu-id="2eb0d-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="2eb0d-112">Der erste Befehl ruft den Tresor mit dem Namen TestVault ab und speichert ihn dann in der Variablen $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="2eb0d-113">Mit dem zweiten Befehl wird die $CredsPath-Variable auf C:\Downloads. festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="2eb0d-114">Der letzte Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 unter Verwendung der Anmeldeinformationen in $CredsPath für Azure-Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="2eb0d-115">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="2eb0d-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="2eb0d-116">Der Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 des Vault-Typs siteRecovery ab.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="2eb0d-117">Beispiel 3: Registrieren eines Windows-Servers oder DPM-Computers für Azure-Sicherung</span><span class="sxs-lookup"><span data-stu-id="2eb0d-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="2eb0d-118">Der Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 ab.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="2eb0d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="2eb0d-119">PARAMETERS</span></span>

### <span data-ttu-id="2eb0d-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="2eb0d-120">-Backup</span></span>
<span data-ttu-id="2eb0d-121">Gibt an, dass die Vault-Anmeldeinformationsdatei auf Azure Backup anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb0d-122">-Path</span><span class="sxs-lookup"><span data-stu-id="2eb0d-122">-Path</span></span>
<span data-ttu-id="2eb0d-123">Gibt den Pfad zur Azure Site Recovery Vault Settings-Datei an.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-123">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="2eb0d-124">Sie können diese Datei vom Azure Site Recovery Vault-Portal herunterladen und lokal speichern.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-124">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb0d-125">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2eb0d-125">-SiteFriendlyName</span></span>
<span data-ttu-id="2eb0d-126">Gibt den Anzeigenamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-126">Specifies the site friendly name.</span></span>
<span data-ttu-id="2eb0d-127">Verwenden Sie diesen Parameter, wenn Sie die Vault-Anmeldeinformationen für eine Hyper-V-Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-127">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb0d-128">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="2eb0d-128">-SiteIdentifier</span></span>
<span data-ttu-id="2eb0d-129">Gibt die Website-ID an.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-129">Specifies the site identifier.</span></span>
<span data-ttu-id="2eb0d-130">Verwenden Sie diesen Parameter, wenn Sie die Vault-Anmeldeinformationen für eine Hyper-V-Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-130">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb0d-131">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2eb0d-131">-SiteRecovery</span></span>
<span data-ttu-id="2eb0d-132">Gibt an, dass die Vault-Anmeldeinformationsdatei auf Azure Site Recovery anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-132">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb0d-133">-Vault</span><span class="sxs-lookup"><span data-stu-id="2eb0d-133">-Vault</span></span>
<span data-ttu-id="2eb0d-134">Gibt das Azure Site Recovery Vault-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-134">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb0d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb0d-135">-DefaultProfile</span></span>
<span data-ttu-id="2eb0d-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eb0d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb0d-137">CommonParameters</span></span>
<span data-ttu-id="2eb0d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb0d-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eb0d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb0d-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2eb0d-140">INPUTS</span></span>

### <span data-ttu-id="2eb0d-141">ARSVault</span><span class="sxs-lookup"><span data-stu-id="2eb0d-141">ARSVault</span></span>
<span data-ttu-id="2eb0d-142">Der Parameter "Vault" akzeptiert den Wert vom Typ "ARSVault" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2eb0d-142">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="2eb0d-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2eb0d-143">OUTPUTS</span></span>

### <span data-ttu-id="2eb0d-144">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="2eb0d-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="2eb0d-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2eb0d-145">NOTES</span></span>

## <span data-ttu-id="2eb0d-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2eb0d-146">RELATED LINKS</span></span>

[<span data-ttu-id="2eb0d-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2eb0d-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="2eb0d-148">Neu – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2eb0d-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="2eb0d-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2eb0d-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


