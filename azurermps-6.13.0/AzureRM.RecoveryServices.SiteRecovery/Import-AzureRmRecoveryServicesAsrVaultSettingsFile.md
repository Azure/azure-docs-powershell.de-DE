---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/import-azurermrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: 7bb92a55f366d90eb5993cfe1520d1b516214372
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477806"
---
# <span data-ttu-id="1300f-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1300f-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="1300f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1300f-102">SYNOPSIS</span></span>
<span data-ttu-id="1300f-103">Importiert die angegebene Datei für ASR Vault-Einstellungen, um den Vault-Kontext (PowerShell-Sitzungskontext) für nachfolgende ASR-Vorgänge in der PowerShell-Sitzung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1300f-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1300f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1300f-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1300f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1300f-105">DESCRIPTION</span></span>
<span data-ttu-id="1300f-106">Mit dem Cmdlet " **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** " wird die Azure Site Recovery Vault-Einstellungsdatei importiert.</span><span class="sxs-lookup"><span data-stu-id="1300f-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="1300f-107">Die Vault-Einstellungsdatei wird verwendet, um den Vault-Kontext für nachfolgende Azure Site Recovery-Vorgänge in der aktuellen Sitzung zu definieren.</span><span class="sxs-lookup"><span data-stu-id="1300f-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="1300f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1300f-108">EXAMPLES</span></span>

### <span data-ttu-id="1300f-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1300f-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="1300f-110">Importiert die angegebene Vault Settings-Datei für Wiederherstellungsdienste und gibt die Einstellungen des importierten Tresors zurück.</span><span class="sxs-lookup"><span data-stu-id="1300f-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="1300f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1300f-111">PARAMETERS</span></span>

### <span data-ttu-id="1300f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1300f-112">-DefaultProfile</span></span>
<span data-ttu-id="1300f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1300f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1300f-114">-Path</span><span class="sxs-lookup"><span data-stu-id="1300f-114">-Path</span></span>
<span data-ttu-id="1300f-115">Gibt den Ordnerpfad der ASR-Tresor-Einstellungsdatei an.</span><span class="sxs-lookup"><span data-stu-id="1300f-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="1300f-116">Diese Datei kann aus dem Vault-Portal für Recovery Services heruntergeladen und lokal gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1300f-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1300f-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1300f-117">-Confirm</span></span>
<span data-ttu-id="1300f-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1300f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1300f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1300f-119">-WhatIf</span></span>
<span data-ttu-id="1300f-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1300f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1300f-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1300f-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1300f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1300f-122">CommonParameters</span></span>
<span data-ttu-id="1300f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1300f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1300f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1300f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1300f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1300f-125">INPUTS</span></span>

### <span data-ttu-id="1300f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1300f-126">System.String</span></span>

## <span data-ttu-id="1300f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1300f-127">OUTPUTS</span></span>

### <span data-ttu-id="1300f-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="1300f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="1300f-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="1300f-129">NOTES</span></span>

## <span data-ttu-id="1300f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1300f-130">RELATED LINKS</span></span>

[<span data-ttu-id="1300f-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1300f-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
