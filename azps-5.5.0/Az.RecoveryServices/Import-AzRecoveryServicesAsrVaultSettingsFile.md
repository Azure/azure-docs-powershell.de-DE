---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: de3604a4bf1f9c46bf88b2f3cda25982672e9096
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160145"
---
# <span data-ttu-id="0d675-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0d675-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="0d675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d675-102">SYNOPSIS</span></span>
<span data-ttu-id="0d675-103">Importiert die angegebene Datei mit den Einstellungen für den ASR-Tresor, um den Tresorkontext (PowerShell-Sitzungskontext) für nachfolgende ASR-Vorgänge in der PowerShell-Sitzung zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="0d675-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="0d675-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d675-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d675-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d675-105">DESCRIPTION</span></span>
<span data-ttu-id="0d675-106">Das **Cmdlet "Import-AzRecoveryServicesAsrVaultSettingsFile"** importiert die Einstellungsdatei für den Azure Site Recovery-Tresor.</span><span class="sxs-lookup"><span data-stu-id="0d675-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="0d675-107">Die Datei mit den Tresoreinstellungen wird verwendet, um den Tresorkontext für nachfolgende Azure-Websitewiederherstellungsvorgänge in der aktuellen Sitzung festlegen.</span><span class="sxs-lookup"><span data-stu-id="0d675-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="0d675-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d675-108">EXAMPLES</span></span>

### <span data-ttu-id="0d675-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d675-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="0d675-110">Importiert die angegebene Einstellungsdatei für den Wiederherstellungsdiensttresor und gibt die Einstellungen des importierten Tresors zurück.</span><span class="sxs-lookup"><span data-stu-id="0d675-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="0d675-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d675-111">PARAMETERS</span></span>

### <span data-ttu-id="0d675-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d675-112">-DefaultProfile</span></span>
<span data-ttu-id="0d675-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d675-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0d675-114">-Path</span><span class="sxs-lookup"><span data-stu-id="0d675-114">-Path</span></span>
<span data-ttu-id="0d675-115">Gibt den Ordnerpfad der Datei mit den Einstellungen für den ASR-Tresor an.</span><span class="sxs-lookup"><span data-stu-id="0d675-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="0d675-116">Diese Datei kann aus dem Wiederherstellungsverwaltungsportal heruntergeladen und lokal gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0d675-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="0d675-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d675-117">-Confirm</span></span>
<span data-ttu-id="0d675-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d675-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d675-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0d675-119">-WhatIf</span></span>
<span data-ttu-id="0d675-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d675-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d675-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d675-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d675-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d675-122">CommonParameters</span></span>
<span data-ttu-id="0d675-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d675-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d675-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d675-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d675-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d675-125">INPUTS</span></span>

### <span data-ttu-id="0d675-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0d675-126">System.String</span></span>

## <span data-ttu-id="0d675-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d675-127">OUTPUTS</span></span>

### <span data-ttu-id="0d675-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="0d675-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="0d675-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0d675-129">NOTES</span></span>

## <span data-ttu-id="0d675-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0d675-130">RELATED LINKS</span></span>

[<span data-ttu-id="0d675-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0d675-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
