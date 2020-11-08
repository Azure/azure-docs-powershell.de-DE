---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: de3604a4bf1f9c46bf88b2f3cda25982672e9096
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007896"
---
# <span data-ttu-id="72113-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="72113-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="72113-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72113-102">SYNOPSIS</span></span>
<span data-ttu-id="72113-103">Importiert die angegebene Datei für ASR Vault-Einstellungen, um den Vault-Kontext (PowerShell-Sitzungskontext) für nachfolgende ASR-Vorgänge in der PowerShell-Sitzung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="72113-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="72113-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72113-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72113-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72113-105">DESCRIPTION</span></span>
<span data-ttu-id="72113-106">Mit dem Cmdlet " **Import-AzRecoveryServicesAsrVaultSettingsFile** " wird die Azure Site Recovery Vault-Einstellungsdatei importiert.</span><span class="sxs-lookup"><span data-stu-id="72113-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="72113-107">Die Vault-Einstellungsdatei wird verwendet, um den Vault-Kontext für nachfolgende Azure Site Recovery-Vorgänge in der aktuellen Sitzung zu definieren.</span><span class="sxs-lookup"><span data-stu-id="72113-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="72113-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72113-108">EXAMPLES</span></span>

### <span data-ttu-id="72113-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72113-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="72113-110">Importiert die angegebene Vault Settings-Datei für Wiederherstellungsdienste und gibt die Einstellungen des importierten Tresors zurück.</span><span class="sxs-lookup"><span data-stu-id="72113-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="72113-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="72113-111">PARAMETERS</span></span>

### <span data-ttu-id="72113-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72113-112">-DefaultProfile</span></span>
<span data-ttu-id="72113-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72113-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="72113-114">-Path</span><span class="sxs-lookup"><span data-stu-id="72113-114">-Path</span></span>
<span data-ttu-id="72113-115">Gibt den Ordnerpfad der ASR-Tresor-Einstellungsdatei an.</span><span class="sxs-lookup"><span data-stu-id="72113-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="72113-116">Diese Datei kann aus dem Vault-Portal für Recovery Services heruntergeladen und lokal gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="72113-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="72113-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72113-117">-Confirm</span></span>
<span data-ttu-id="72113-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72113-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72113-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72113-119">-WhatIf</span></span>
<span data-ttu-id="72113-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72113-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72113-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72113-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72113-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72113-122">CommonParameters</span></span>
<span data-ttu-id="72113-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72113-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72113-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72113-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72113-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72113-125">INPUTS</span></span>

### <span data-ttu-id="72113-126">System. String</span><span class="sxs-lookup"><span data-stu-id="72113-126">System.String</span></span>

## <span data-ttu-id="72113-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72113-127">OUTPUTS</span></span>

### <span data-ttu-id="72113-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="72113-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="72113-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="72113-129">NOTES</span></span>

## <span data-ttu-id="72113-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72113-130">RELATED LINKS</span></span>

[<span data-ttu-id="72113-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="72113-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
