---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 3d0761ff05a0cdcd775a234b4da0a50d27c2ba08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477786"
---
# <span data-ttu-id="28514-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="28514-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="28514-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28514-102">SYNOPSIS</span></span>
<span data-ttu-id="28514-103">Legt den Vault-Kontext für Wiederherstellungsdienste für nachfolgende Azure Site Recovery-Vorgänge in der aktuellen PowerShell-Sitzung fest.</span><span class="sxs-lookup"><span data-stu-id="28514-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28514-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28514-104">SYNTAX</span></span>

### <span data-ttu-id="28514-105">AzureRecoveryServicesVault (Standard)</span><span class="sxs-lookup"><span data-stu-id="28514-105">AzureRecoveryServicesVault (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28514-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="28514-106">ByResourceId</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28514-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28514-107">DESCRIPTION</span></span>
<span data-ttu-id="28514-108">Das Cmdlet " **Set-AzureRmRecoveryServicesAsrVaultContext** " legt den Azure Site Recovery Vault-Kontext für weitere Vorgänge fest.</span><span class="sxs-lookup"><span data-stu-id="28514-108">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="28514-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28514-109">EXAMPLES</span></span>

### <span data-ttu-id="28514-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28514-110">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="28514-111">Legt den Vault-Kontext auf den angegebenen Recovery Services Vault für nachfolgende Azure Site Recovery-Vorgänge in der aktuellen PowerShell-Sitzung fest.</span><span class="sxs-lookup"><span data-stu-id="28514-111">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="28514-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="28514-112">PARAMETERS</span></span>

### <span data-ttu-id="28514-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28514-113">-DefaultProfile</span></span>
<span data-ttu-id="28514-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28514-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28514-115">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="28514-115">-ResourceId</span></span>
<span data-ttu-id="28514-116">Gibt die recoveryservices-Tresor-Ressourcen-ID an, die als Vault-Kontext festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="28514-116">Specifies the recoveryservices vault resource id to be set as Vault context.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28514-117">-Vault</span><span class="sxs-lookup"><span data-stu-id="28514-117">-Vault</span></span>
<span data-ttu-id="28514-118">Das Vault-Objekt für Wiederherstellungsdienste, das dem Speicher für Wiederherstellungsdienste entspricht.</span><span class="sxs-lookup"><span data-stu-id="28514-118">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28514-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28514-119">-Confirm</span></span>
<span data-ttu-id="28514-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28514-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28514-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28514-121">-WhatIf</span></span>
<span data-ttu-id="28514-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28514-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28514-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28514-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28514-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28514-124">CommonParameters</span></span>
<span data-ttu-id="28514-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28514-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28514-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28514-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28514-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28514-127">INPUTS</span></span>

### <span data-ttu-id="28514-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="28514-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="28514-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28514-129">OUTPUTS</span></span>

### <span data-ttu-id="28514-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="28514-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="28514-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="28514-131">NOTES</span></span>

## <span data-ttu-id="28514-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28514-132">RELATED LINKS</span></span>
