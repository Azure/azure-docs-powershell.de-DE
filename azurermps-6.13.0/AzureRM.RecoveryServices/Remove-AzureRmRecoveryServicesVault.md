---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: e6ac59a84e4244cb6d6815f8e3256618cccd661c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503430"
---
# <span data-ttu-id="46ec5-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="46ec5-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="46ec5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="46ec5-103">Löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="46ec5-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46ec5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46ec5-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46ec5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="46ec5-106">Das Cmdlet **Remove-AzureRmRecoveryServicesVault** löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="46ec5-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="46ec5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="46ec5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46ec5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="46ec5-109">Löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="46ec5-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="46ec5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46ec5-110">PARAMETERS</span></span>

### <span data-ttu-id="46ec5-111">-Vault</span><span class="sxs-lookup"><span data-stu-id="46ec5-111">-Vault</span></span>
<span data-ttu-id="46ec5-112">Gibt ein Azure Site Recovery Vault-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="46ec5-112">Specifies an Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46ec5-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46ec5-113">-Confirm</span></span>
<span data-ttu-id="46ec5-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46ec5-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46ec5-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46ec5-115">-WhatIf</span></span>
<span data-ttu-id="46ec5-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46ec5-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46ec5-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46ec5-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46ec5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ec5-118">-DefaultProfile</span></span>
<span data-ttu-id="46ec5-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46ec5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46ec5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ec5-120">CommonParameters</span></span>
<span data-ttu-id="46ec5-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ec5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ec5-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ec5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ec5-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46ec5-123">INPUTS</span></span>

### <span data-ttu-id="46ec5-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="46ec5-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="46ec5-125">Parameter: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46ec5-125">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="46ec5-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46ec5-126">OUTPUTS</span></span>

### <span data-ttu-id="46ec5-127">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="46ec5-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="46ec5-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="46ec5-128">NOTES</span></span>

## <span data-ttu-id="46ec5-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46ec5-129">RELATED LINKS</span></span>

[<span data-ttu-id="46ec5-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="46ec5-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="46ec5-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="46ec5-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="46ec5-132">Neu – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="46ec5-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


