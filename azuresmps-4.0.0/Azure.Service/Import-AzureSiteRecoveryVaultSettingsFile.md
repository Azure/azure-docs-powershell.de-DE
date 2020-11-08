---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006466"
---
# <span data-ttu-id="f1775-101">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f1775-101">Import-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="f1775-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1775-102">SYNOPSIS</span></span>
<span data-ttu-id="f1775-103">Importiert eine Vault-Einstellungsdatei für eine Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="f1775-103">Imports a Site Recovery vault settings file.</span></span>

## <span data-ttu-id="f1775-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1775-104">SYNTAX</span></span>

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f1775-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1775-105">DESCRIPTION</span></span>
<span data-ttu-id="f1775-106">Das Cmdlet " **Import-AzureSiteRecoveryVaultSettingsFile** " importiert eine Azure Site Recovery Vault Settings-Datei, um den Vault-Kontext für nachfolgende Website Wiederherstellungsvorgänge in der aktuellen Sitzung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f1775-106">The **Import-AzureSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="f1775-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1775-107">EXAMPLES</span></span>

### <span data-ttu-id="f1775-108">Beispiel 1: Importieren einer Tresor-Einstellungsdatei</span><span class="sxs-lookup"><span data-stu-id="f1775-108">Example 1: Import a vault settings file</span></span>
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="f1775-109">Mit diesem Befehl wird die Vault Settings-Datei im angegebenen Pfad importiert.</span><span class="sxs-lookup"><span data-stu-id="f1775-109">This command imports the vault settings file at the specified path.</span></span>

## <span data-ttu-id="f1775-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1775-110">PARAMETERS</span></span>

### <span data-ttu-id="f1775-111">-Path</span><span class="sxs-lookup"><span data-stu-id="f1775-111">-Path</span></span>
<span data-ttu-id="f1775-112">Gibt den Pfad der Datei für die Vault-Einstellungen der Websitewiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="f1775-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="f1775-113">Diese Datei kann aus dem Vault-Portal der Websitewiederherstellung heruntergeladen und lokal gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f1775-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1775-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="f1775-114">-Profile</span></span>
<span data-ttu-id="f1775-115">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f1775-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f1775-116">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f1775-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f1775-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1775-117">CommonParameters</span></span>
<span data-ttu-id="f1775-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1775-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1775-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1775-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1775-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1775-120">INPUTS</span></span>

## <span data-ttu-id="f1775-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1775-121">OUTPUTS</span></span>

## <span data-ttu-id="f1775-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1775-122">NOTES</span></span>

## <span data-ttu-id="f1775-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1775-123">RELATED LINKS</span></span>

[<span data-ttu-id="f1775-124">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="f1775-124">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="f1775-125">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f1775-125">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)


