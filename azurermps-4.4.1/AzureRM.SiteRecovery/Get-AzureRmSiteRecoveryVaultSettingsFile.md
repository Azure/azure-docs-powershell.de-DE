---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 242dfd46b179d1e7d55613d938eddf5b691da6c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664719"
---
# <span data-ttu-id="70373-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="70373-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="70373-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70373-102">SYNOPSIS</span></span>
<span data-ttu-id="70373-103">Ruft die Datei für die Vault-Einstellungen der Websitewiederherstellung ab.</span><span class="sxs-lookup"><span data-stu-id="70373-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70373-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70373-104">SYNTAX</span></span>

### <span data-ttu-id="70373-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="70373-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70373-106">Standard</span><span class="sxs-lookup"><span data-stu-id="70373-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70373-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="70373-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70373-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70373-108">DESCRIPTION</span></span>
<span data-ttu-id="70373-109">Das Cmdlet " **Get-AzureRmSiteRecoveryVaultSettingsFile** " Ruft die Einstellungsdatei für ein Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="70373-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="70373-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70373-110">EXAMPLES</span></span>

## <span data-ttu-id="70373-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="70373-111">PARAMETERS</span></span>

### <span data-ttu-id="70373-112">-Path</span><span class="sxs-lookup"><span data-stu-id="70373-112">-Path</span></span>
<span data-ttu-id="70373-113">Gibt den Pfad zur Website Recovery Vault Settings-Datei an.</span><span class="sxs-lookup"><span data-stu-id="70373-113">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="70373-114">Wenn Sie diese Datei lokal speichern möchten, laden Sie Sie nach Abschluss des Befehls aus dem Vault-Portal der Website wieder her.</span><span class="sxs-lookup"><span data-stu-id="70373-114">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70373-115">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="70373-115">-SiteFriendlyName</span></span>
<span data-ttu-id="70373-116">Gibt den Website Anzeigenamen für den Tresor an, wenn es sich um eine Hyper-V-Website handelt.</span><span class="sxs-lookup"><span data-stu-id="70373-116">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="70373-117">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="70373-117">-SiteIdentifier</span></span>
<span data-ttu-id="70373-118">Gibt die Website-ID für den Tresor an, wenn es sich um eine Hyper-V-Website handelt.</span><span class="sxs-lookup"><span data-stu-id="70373-118">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="70373-119">-Vault</span><span class="sxs-lookup"><span data-stu-id="70373-119">-Vault</span></span>
<span data-ttu-id="70373-120">Gibt das Vault-Objekt für die Website an.</span><span class="sxs-lookup"><span data-stu-id="70373-120">Specifies the vault object for the site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70373-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70373-121">-DefaultProfile</span></span>
<span data-ttu-id="70373-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70373-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70373-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70373-123">CommonParameters</span></span>
<span data-ttu-id="70373-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70373-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70373-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70373-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70373-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70373-126">INPUTS</span></span>

### <span data-ttu-id="70373-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="70373-127">ASRVault</span></span>
<span data-ttu-id="70373-128">Der Parameter "Vault" akzeptiert den Wert vom Typ "ASRVault" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="70373-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="70373-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70373-129">OUTPUTS</span></span>

### <span data-ttu-id="70373-130">Microsoft. Azure. Commands. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="70373-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="70373-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="70373-131">NOTES</span></span>

## <span data-ttu-id="70373-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70373-132">RELATED LINKS</span></span>

[<span data-ttu-id="70373-133">Importieren-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="70373-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="70373-134">Satz-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="70373-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
