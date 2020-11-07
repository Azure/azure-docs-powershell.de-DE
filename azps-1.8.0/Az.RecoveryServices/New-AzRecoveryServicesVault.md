---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 65694116a924759c4cf29a7abcf95da7a03df39f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659855"
---
# <span data-ttu-id="9ef0e-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9ef0e-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="9ef0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ef0e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef0e-103">Erstellt einen neuen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="9ef0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ef0e-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ef0e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ef0e-105">DESCRIPTION</span></span>
<span data-ttu-id="9ef0e-106">Das Cmdlet **New-AzRecoveryServicesVault** erstellt einen neuen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="9ef0e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ef0e-107">EXAMPLES</span></span>

### <span data-ttu-id="9ef0e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ef0e-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="9ef0e-109">Erstellen des Wiederherstellungs Dienst Depots in der Ressourcengruppe und dem angegebenen Speicherort</span><span class="sxs-lookup"><span data-stu-id="9ef0e-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="9ef0e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ef0e-110">PARAMETERS</span></span>

### <span data-ttu-id="9ef0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef0e-111">-DefaultProfile</span></span>
<span data-ttu-id="9ef0e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ef0e-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="9ef0e-113">-Location</span></span>
<span data-ttu-id="9ef0e-114">Gibt den Namen des geografischen Speicherorts des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="9ef0e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9ef0e-115">-Name</span></span>
<span data-ttu-id="9ef0e-116">Gibt den Namen des zu erstellende Vault an.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="9ef0e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef0e-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ef0e-118">Gibt den Namen der Azure-Ressourcengruppe an, in der erstellt werden soll, oder aus der das angegebene Wiederherstellungsdienste-Objekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="9ef0e-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ef0e-119">-Confirm</span></span>
<span data-ttu-id="9ef0e-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef0e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef0e-121">-WhatIf</span></span>
<span data-ttu-id="9ef0e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ef0e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef0e-124">CommonParameters</span></span>
<span data-ttu-id="9ef0e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef0e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ef0e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef0e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ef0e-127">INPUTS</span></span>

### <span data-ttu-id="9ef0e-128">Keine</span><span class="sxs-lookup"><span data-stu-id="9ef0e-128">None</span></span>

## <span data-ttu-id="9ef0e-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ef0e-129">OUTPUTS</span></span>

### <span data-ttu-id="9ef0e-130">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="9ef0e-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9ef0e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ef0e-131">NOTES</span></span>

## <span data-ttu-id="9ef0e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ef0e-132">RELATED LINKS</span></span>

[<span data-ttu-id="9ef0e-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9ef0e-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="9ef0e-134">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9ef0e-134">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="9ef0e-135">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9ef0e-135">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


