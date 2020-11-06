---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: d9163e42b199dd5178e37a7d1bbe22abbb05c7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478997"
---
# <span data-ttu-id="abc1d-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="abc1d-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="abc1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="abc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="abc1d-103">Erstellt einen neuen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="abc1d-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abc1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="abc1d-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc1d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abc1d-105">DESCRIPTION</span></span>
<span data-ttu-id="abc1d-106">Das Cmdlet **New-AzureRmRecoveryServicesVault** erstellt einen neuen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="abc1d-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="abc1d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abc1d-107">EXAMPLES</span></span>

## <span data-ttu-id="abc1d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="abc1d-108">PARAMETERS</span></span>

### <span data-ttu-id="abc1d-109">-Standort</span><span class="sxs-lookup"><span data-stu-id="abc1d-109">-Location</span></span>
<span data-ttu-id="abc1d-110">Gibt den Namen des geografischen Speicherorts des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="abc1d-110">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc1d-111">-Name</span><span class="sxs-lookup"><span data-stu-id="abc1d-111">-Name</span></span>
<span data-ttu-id="abc1d-112">Gibt den Namen des zu erstellende Vault an.</span><span class="sxs-lookup"><span data-stu-id="abc1d-112">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc1d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc1d-113">-ResourceGroupName</span></span>
<span data-ttu-id="abc1d-114">Gibt den Namen der Azure-Ressourcengruppe an, in der erstellt werden soll, oder aus der das angegebene Wiederherstellungsdienste-Objekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="abc1d-114">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc1d-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="abc1d-115">-Confirm</span></span>
<span data-ttu-id="abc1d-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abc1d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc1d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc1d-117">-WhatIf</span></span>
<span data-ttu-id="abc1d-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc1d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abc1d-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abc1d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc1d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc1d-120">-DefaultProfile</span></span>
<span data-ttu-id="abc1d-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="abc1d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abc1d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc1d-122">CommonParameters</span></span>
<span data-ttu-id="abc1d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc1d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc1d-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc1d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc1d-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="abc1d-125">INPUTS</span></span>

## <span data-ttu-id="abc1d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="abc1d-126">OUTPUTS</span></span>

### <span data-ttu-id="abc1d-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="abc1d-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="abc1d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="abc1d-128">NOTES</span></span>

## <span data-ttu-id="abc1d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="abc1d-129">RELATED LINKS</span></span>

[<span data-ttu-id="abc1d-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="abc1d-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="abc1d-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="abc1d-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="abc1d-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="abc1d-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


