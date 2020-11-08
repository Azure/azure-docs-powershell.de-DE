---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006770"
---
# <span data-ttu-id="ae4ea-101">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ae4ea-101">Get-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="ae4ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4ea-103">Ruft die Datei für die Vault-Einstellungen der Websitewiederherstellung ab.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-103">Gets the Site Recovery vault settings file.</span></span>

## <span data-ttu-id="ae4ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae4ea-104">SYNTAX</span></span>

### <span data-ttu-id="ae4ea-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae4ea-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ae4ea-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="ae4ea-106">ByObject</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae4ea-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae4ea-107">DESCRIPTION</span></span>
<span data-ttu-id="ae4ea-108">Das Cmdlet " **Get-AzureSiteRecoveryVaultSettingsFile** " Ruft die Einstellungsdatei für ein Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-108">The **Get-AzureSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="ae4ea-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae4ea-109">EXAMPLES</span></span>

### <span data-ttu-id="ae4ea-110">Beispiel 1: Abrufen der Einstellungsdatei für einen Tresor</span><span class="sxs-lookup"><span data-stu-id="ae4ea-110">Example 1: Get the settings file for a vault</span></span>
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

<span data-ttu-id="ae4ea-111">Der erste Befehl ruft das Active Azure Site Recovery Vault mit dem Namen ContosoVault mit dem Cmdlet **Get-AzureSiteRecoveryVault** ab.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-111">The first command gets the active Azure Site Recovery vault named ContosoVault by using the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>
<span data-ttu-id="ae4ea-112">Der Befehl speichert diesen Tresor in der $Vault-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-112">The command stores that vault in the $Vault variable.</span></span>

<span data-ttu-id="ae4ea-113">Der zweite Befehl ruft die Einstellungsdatei für den Tresor ab, der in $Vault gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-113">The second command gets the settings file for the vault stored in $Vault.</span></span>

## <span data-ttu-id="ae4ea-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae4ea-114">PARAMETERS</span></span>

### <span data-ttu-id="ae4ea-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="ae4ea-115">-Location</span></span>
<span data-ttu-id="ae4ea-116">Gibt den geografischen Standort an, zu dem der Tresor gehört.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-116">Specifies the geographical location to which the vault belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ea-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ae4ea-117">-Name</span></span>
<span data-ttu-id="ae4ea-118">Gibt den Namen eines Tresors an.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-118">Specifies the name of a vault.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ea-119">-Path</span><span class="sxs-lookup"><span data-stu-id="ae4ea-119">-Path</span></span>
<span data-ttu-id="ae4ea-120">Gibt den Pfad der Datei für die Vault-Einstellungen der Websitewiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-120">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="ae4ea-121">Wenn Sie diese Datei lokal speichern möchten, laden Sie Sie aus dem Vault-Portal der Standortwiederherstellung herunter, nachdem der Befehl ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-121">To store this file locally, download it from the Site Recovery vault portal after the command has finished running.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ea-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="ae4ea-122">-Profile</span></span>
<span data-ttu-id="ae4ea-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae4ea-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ea-125">-Website</span><span class="sxs-lookup"><span data-stu-id="ae4ea-125">-Site</span></span>
<span data-ttu-id="ae4ea-126">Gibt eine Website an, für die eine Einstellungsdatei abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-126">Specifies a site for which to get a settings file.</span></span>
<span data-ttu-id="ae4ea-127">Verwenden Sie zum Abrufen eines **Website** Objekts das Cmdlet **Get-AzureSiteRecoverySite** .</span><span class="sxs-lookup"><span data-stu-id="ae4ea-127">To obtain a **Site** object, use the **Get-AzureSiteRecoverySite** cmdlet.</span></span>

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ea-128">-Standort-Nr</span><span class="sxs-lookup"><span data-stu-id="ae4ea-128">-SiteId</span></span>
<span data-ttu-id="ae4ea-129">Gibt die ID einer Website an.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-129">Specifies the ID of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ea-130">-Sitename</span><span class="sxs-lookup"><span data-stu-id="ae4ea-130">-SiteName</span></span>
<span data-ttu-id="ae4ea-131">Gibt den Namen einer Website an.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-131">Specifies the name of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ea-132">-Vault</span><span class="sxs-lookup"><span data-stu-id="ae4ea-132">-Vault</span></span>
<span data-ttu-id="ae4ea-133">Gibt den Tresor für die Website an.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-133">Specifies the vault for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4ea-134">CommonParameters</span></span>
<span data-ttu-id="ae4ea-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4ea-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae4ea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4ea-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae4ea-137">INPUTS</span></span>

## <span data-ttu-id="ae4ea-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae4ea-138">OUTPUTS</span></span>

## <span data-ttu-id="ae4ea-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae4ea-139">NOTES</span></span>

## <span data-ttu-id="ae4ea-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae4ea-140">RELATED LINKS</span></span>

[<span data-ttu-id="ae4ea-141">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="ae4ea-141">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)

[<span data-ttu-id="ae4ea-142">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="ae4ea-142">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="ae4ea-143">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="ae4ea-143">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="ae4ea-144">Importieren-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ae4ea-144">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


