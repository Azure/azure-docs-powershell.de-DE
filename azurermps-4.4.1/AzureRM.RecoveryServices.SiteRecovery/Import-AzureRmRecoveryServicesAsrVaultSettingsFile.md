---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662631"
---
# <span data-ttu-id="ba16c-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ba16c-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="ba16c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba16c-102">SYNOPSIS</span></span>
<span data-ttu-id="ba16c-103">Importiert die angegebene Datei für ASR Vault-Einstellungen, um den Vault-Kontext (PowerShell-Sitzungskontext) für nachfolgende ASR-Vorgänge in der PowerShell-Sitzung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ba16c-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba16c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba16c-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba16c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba16c-105">DESCRIPTION</span></span>
<span data-ttu-id="ba16c-106">Mit dem Cmdlet " **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** " wird die Azure Site Recovery Vault-Einstellungsdatei importiert.</span><span class="sxs-lookup"><span data-stu-id="ba16c-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="ba16c-107">Die Vault-Einstellungsdatei wird verwendet, um den Vault-Kontext für nachfolgende Azure Site Recovery-Vorgänge in der aktuellen Sitzung zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ba16c-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="ba16c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba16c-108">EXAMPLES</span></span>

### <span data-ttu-id="ba16c-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba16c-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="ba16c-110">Importiert die angegebene Vault Settings-Datei für Wiederherstellungsdienste und gibt die Einstellungen des importierten Tresors zurück.</span><span class="sxs-lookup"><span data-stu-id="ba16c-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="ba16c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba16c-111">PARAMETERS</span></span>

### <span data-ttu-id="ba16c-112">-Path</span><span class="sxs-lookup"><span data-stu-id="ba16c-112">-Path</span></span>
<span data-ttu-id="ba16c-113">Gibt den Pfad der ASR-Tresor-Einstellungsdatei an.</span><span class="sxs-lookup"><span data-stu-id="ba16c-113">Specifies the path of the ASR vault settings file.</span></span>
<span data-ttu-id="ba16c-114">Diese Datei kann aus dem Vault-Portal für Recovery Services heruntergeladen und lokal gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ba16c-114">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="ba16c-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba16c-115">-Confirm</span></span>
<span data-ttu-id="ba16c-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba16c-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba16c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba16c-117">-WhatIf</span></span>
<span data-ttu-id="ba16c-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba16c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba16c-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba16c-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba16c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba16c-120">CommonParameters</span></span>
<span data-ttu-id="ba16c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba16c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba16c-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba16c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba16c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba16c-123">INPUTS</span></span>

### <span data-ttu-id="ba16c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ba16c-124">System.String</span></span>

## <span data-ttu-id="ba16c-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba16c-125">OUTPUTS</span></span>

### <span data-ttu-id="ba16c-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="ba16c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="ba16c-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba16c-127">NOTES</span></span>

## <span data-ttu-id="ba16c-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba16c-128">RELATED LINKS</span></span>

[<span data-ttu-id="ba16c-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ba16c-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
