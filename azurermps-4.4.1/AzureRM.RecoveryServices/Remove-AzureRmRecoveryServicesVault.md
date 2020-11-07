---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: b3df84865d29bbcf62074c1b1ed7f5586fb64fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663846"
---
# <span data-ttu-id="3b2ea-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3b2ea-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="3b2ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="3b2ea-103">Löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="3b2ea-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b2ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b2ea-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b2ea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b2ea-105">DESCRIPTION</span></span>
<span data-ttu-id="3b2ea-106">Das Cmdlet **Remove-AzureRmRecoveryServicesVault** löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="3b2ea-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="3b2ea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b2ea-107">EXAMPLES</span></span>

## <span data-ttu-id="3b2ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b2ea-108">PARAMETERS</span></span>

### <span data-ttu-id="3b2ea-109">-Vault</span><span class="sxs-lookup"><span data-stu-id="3b2ea-109">-Vault</span></span>
<span data-ttu-id="3b2ea-110">Gibt ein Azure Site Recovery Vault-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3b2ea-110">Specifies an Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2ea-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b2ea-111">-Confirm</span></span>
<span data-ttu-id="3b2ea-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b2ea-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b2ea-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b2ea-113">-WhatIf</span></span>
<span data-ttu-id="3b2ea-114">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b2ea-114">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b2ea-115">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b2ea-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b2ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b2ea-116">-DefaultProfile</span></span>
<span data-ttu-id="3b2ea-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b2ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b2ea-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b2ea-118">CommonParameters</span></span>
<span data-ttu-id="3b2ea-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b2ea-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b2ea-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b2ea-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b2ea-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b2ea-121">INPUTS</span></span>

### <span data-ttu-id="3b2ea-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="3b2ea-122">ARSVault</span></span>
<span data-ttu-id="3b2ea-123">Der Parameter "Vault" akzeptiert den Wert vom Typ "ARSVault" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3b2ea-123">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="3b2ea-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b2ea-124">OUTPUTS</span></span>

### <span data-ttu-id="3b2ea-125">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="3b2ea-125">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="3b2ea-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b2ea-126">NOTES</span></span>

## <span data-ttu-id="3b2ea-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b2ea-127">RELATED LINKS</span></span>

[<span data-ttu-id="3b2ea-128">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3b2ea-128">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="3b2ea-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3b2ea-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="3b2ea-130">Neu – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3b2ea-130">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


