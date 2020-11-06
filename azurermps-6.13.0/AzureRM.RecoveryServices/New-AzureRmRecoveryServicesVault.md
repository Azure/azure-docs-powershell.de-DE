---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 08166ea1ebe4c78521a68f9e5423a7947e78b699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503433"
---
# <span data-ttu-id="15b52-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="15b52-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="15b52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15b52-102">SYNOPSIS</span></span>
<span data-ttu-id="15b52-103">Erstellt einen neuen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="15b52-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15b52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15b52-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15b52-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15b52-105">DESCRIPTION</span></span>
<span data-ttu-id="15b52-106">Das Cmdlet **New-AzureRmRecoveryServicesVault** erstellt einen neuen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="15b52-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="15b52-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15b52-107">EXAMPLES</span></span>

### <span data-ttu-id="15b52-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="15b52-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="15b52-109">Erstellen des Wiederherstellungs Dienst Depots in der Ressourcengruppe und dem angegebenen Speicherort</span><span class="sxs-lookup"><span data-stu-id="15b52-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="15b52-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="15b52-110">PARAMETERS</span></span>

### <span data-ttu-id="15b52-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="15b52-111">-Location</span></span>
<span data-ttu-id="15b52-112">Gibt den Namen des geografischen Speicherorts des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="15b52-112">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b52-113">-Name</span><span class="sxs-lookup"><span data-stu-id="15b52-113">-Name</span></span>
<span data-ttu-id="15b52-114">Gibt den Namen des zu erstellende Vault an.</span><span class="sxs-lookup"><span data-stu-id="15b52-114">Specifies the name of the vault to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b52-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b52-115">-ResourceGroupName</span></span>
<span data-ttu-id="15b52-116">Gibt den Namen der Azure-Ressourcengruppe an, in der erstellt werden soll, oder aus der das angegebene Wiederherstellungsdienste-Objekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="15b52-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b52-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15b52-117">-Confirm</span></span>
<span data-ttu-id="15b52-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15b52-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15b52-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b52-119">-WhatIf</span></span>
<span data-ttu-id="15b52-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15b52-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15b52-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15b52-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15b52-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b52-122">-DefaultProfile</span></span>
<span data-ttu-id="15b52-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15b52-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15b52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b52-124">CommonParameters</span></span>
<span data-ttu-id="15b52-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b52-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b52-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b52-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15b52-127">INPUTS</span></span>

### <span data-ttu-id="15b52-128">Keine</span><span class="sxs-lookup"><span data-stu-id="15b52-128">None</span></span>

## <span data-ttu-id="15b52-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15b52-129">OUTPUTS</span></span>

### <span data-ttu-id="15b52-130">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="15b52-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="15b52-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="15b52-131">NOTES</span></span>

## <span data-ttu-id="15b52-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15b52-132">RELATED LINKS</span></span>

[<span data-ttu-id="15b52-133">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="15b52-133">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="15b52-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="15b52-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="15b52-135">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="15b52-135">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


