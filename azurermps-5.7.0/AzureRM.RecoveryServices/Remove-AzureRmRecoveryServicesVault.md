---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 4d3046827a7d3338833b0c8c788cfb7a9e18bc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500445"
---
# <span data-ttu-id="11aae-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="11aae-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="11aae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11aae-102">SYNOPSIS</span></span>
<span data-ttu-id="11aae-103">Löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="11aae-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11aae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11aae-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11aae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11aae-105">DESCRIPTION</span></span>
<span data-ttu-id="11aae-106">Das Cmdlet **Remove-AzureRmRecoveryServicesVault** löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="11aae-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="11aae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11aae-107">EXAMPLES</span></span>

### <span data-ttu-id="11aae-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="11aae-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="11aae-109">Löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="11aae-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="11aae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="11aae-110">PARAMETERS</span></span>

### <span data-ttu-id="11aae-111">-Vault</span><span class="sxs-lookup"><span data-stu-id="11aae-111">-Vault</span></span>
<span data-ttu-id="11aae-112">Gibt ein Azure Site Recovery Vault-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="11aae-112">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="11aae-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="11aae-113">-Confirm</span></span>
<span data-ttu-id="11aae-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11aae-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11aae-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11aae-115">-WhatIf</span></span>
<span data-ttu-id="11aae-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11aae-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11aae-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11aae-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11aae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11aae-118">-DefaultProfile</span></span>
<span data-ttu-id="11aae-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11aae-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11aae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11aae-120">CommonParameters</span></span>
<span data-ttu-id="11aae-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11aae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11aae-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11aae-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11aae-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11aae-123">INPUTS</span></span>

### <span data-ttu-id="11aae-124">ARSVault</span><span class="sxs-lookup"><span data-stu-id="11aae-124">ARSVault</span></span>
<span data-ttu-id="11aae-125">Der Parameter "Vault" akzeptiert den Wert vom Typ "ARSVault" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="11aae-125">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="11aae-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11aae-126">OUTPUTS</span></span>

### <span data-ttu-id="11aae-127">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="11aae-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="11aae-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="11aae-128">NOTES</span></span>

## <span data-ttu-id="11aae-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11aae-129">RELATED LINKS</span></span>

[<span data-ttu-id="11aae-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="11aae-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="11aae-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="11aae-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="11aae-132">Neu – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="11aae-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


