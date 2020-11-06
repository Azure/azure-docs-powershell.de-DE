---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501654"
---
# <span data-ttu-id="2898d-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2898d-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="2898d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2898d-102">SYNOPSIS</span></span>
<span data-ttu-id="2898d-103">Ruft die Azure Site Recovery Vault Settings-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="2898d-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2898d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2898d-104">SYNTAX</span></span>

### <span data-ttu-id="2898d-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="2898d-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2898d-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="2898d-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2898d-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="2898d-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2898d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2898d-108">DESCRIPTION</span></span>
<span data-ttu-id="2898d-109">Das Cmdlet " **Get-AzureRmRecoveryServicesVaultSettingsFile** " Ruft die Einstellungsdatei für ein Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="2898d-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="2898d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2898d-110">EXAMPLES</span></span>

### <span data-ttu-id="2898d-111">Beispiel 1: Registrieren eines Windows-Servers oder DPM-Computers für Azure-Sicherung</span><span class="sxs-lookup"><span data-stu-id="2898d-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="2898d-112">Der erste Befehl ruft den Tresor mit dem Namen TestVault ab und speichert ihn dann in der Variablen $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="2898d-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="2898d-113">Mit dem zweiten Befehl wird die $CredsPath-Variable auf C:\Downloads. festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2898d-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="2898d-114">Der letzte Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 unter Verwendung der Anmeldeinformationen in $CredsPath für Azure-Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="2898d-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

## <span data-ttu-id="2898d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2898d-115">PARAMETERS</span></span>

### <span data-ttu-id="2898d-116">-Backup</span><span class="sxs-lookup"><span data-stu-id="2898d-116">-Backup</span></span>
<span data-ttu-id="2898d-117">Gibt an, dass die Vault-Anmeldeinformationsdatei auf Azure Backup anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="2898d-117">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="2898d-118">-Path</span><span class="sxs-lookup"><span data-stu-id="2898d-118">-Path</span></span>
<span data-ttu-id="2898d-119">Gibt den Pfad zur Azure Site Recovery Vault Settings-Datei an.</span><span class="sxs-lookup"><span data-stu-id="2898d-119">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="2898d-120">Sie können diese Datei vom Azure Site Recovery Vault-Portal herunterladen und lokal speichern.</span><span class="sxs-lookup"><span data-stu-id="2898d-120">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="2898d-121">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2898d-121">-SiteFriendlyName</span></span>
<span data-ttu-id="2898d-122">Gibt den Anzeigenamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="2898d-122">Specifies the site friendly name.</span></span>
<span data-ttu-id="2898d-123">Verwenden Sie diesen Parameter, wenn Sie die Vault-Anmeldeinformationen für eine Hyper-V-Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2898d-123">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="2898d-124">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="2898d-124">-SiteIdentifier</span></span>
<span data-ttu-id="2898d-125">Gibt die Website-ID an.</span><span class="sxs-lookup"><span data-stu-id="2898d-125">Specifies the site identifier.</span></span>
<span data-ttu-id="2898d-126">Verwenden Sie diesen Parameter, wenn Sie die Vault-Anmeldeinformationen für eine Hyper-V-Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2898d-126">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="2898d-127">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2898d-127">-SiteRecovery</span></span>
<span data-ttu-id="2898d-128">Gibt an, dass die Vault-Anmeldeinformationsdatei auf Azure Site Recovery anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="2898d-128">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="2898d-129">-Vault</span><span class="sxs-lookup"><span data-stu-id="2898d-129">-Vault</span></span>
<span data-ttu-id="2898d-130">Gibt das Azure Site Recovery Vault-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2898d-130">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="2898d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2898d-131">-DefaultProfile</span></span>
<span data-ttu-id="2898d-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2898d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2898d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2898d-133">CommonParameters</span></span>
<span data-ttu-id="2898d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2898d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2898d-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2898d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2898d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2898d-136">INPUTS</span></span>

### <span data-ttu-id="2898d-137">ARSVault</span><span class="sxs-lookup"><span data-stu-id="2898d-137">ARSVault</span></span>
<span data-ttu-id="2898d-138">Der Parameter "Vault" akzeptiert den Wert vom Typ "ARSVault" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2898d-138">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="2898d-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2898d-139">OUTPUTS</span></span>

### <span data-ttu-id="2898d-140">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="2898d-140">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="2898d-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="2898d-141">NOTES</span></span>

## <span data-ttu-id="2898d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2898d-142">RELATED LINKS</span></span>

[<span data-ttu-id="2898d-143">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2898d-143">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="2898d-144">Neu – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2898d-144">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="2898d-145">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2898d-145">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


