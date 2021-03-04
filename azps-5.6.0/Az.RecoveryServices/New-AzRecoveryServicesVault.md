---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 811ac8b9f8922844dd5153a4fa02abc4c023f7a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919267"
---
# <span data-ttu-id="f9644-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f9644-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="f9644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9644-102">SYNOPSIS</span></span>
<span data-ttu-id="f9644-103">Erstellt einen neuen Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="f9644-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="f9644-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9644-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9644-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9644-105">DESCRIPTION</span></span>
<span data-ttu-id="f9644-106">Das **Cmdlet New-AzRecoveryServicesVault** erstellt einen neuen Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="f9644-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="f9644-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9644-107">EXAMPLES</span></span>

### <span data-ttu-id="f9644-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9644-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="f9644-109">Erstellen Sie den Wiederherstellungsdiensttresor in der Ressourcengruppe und dem angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="f9644-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="f9644-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f9644-110">PARAMETERS</span></span>

### <span data-ttu-id="f9644-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9644-111">-DefaultProfile</span></span>
<span data-ttu-id="f9644-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9644-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9644-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f9644-113">-Location</span></span>
<span data-ttu-id="f9644-114">Gibt den Namen des geografischen Speicherorts des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="f9644-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="f9644-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f9644-115">-Name</span></span>
<span data-ttu-id="f9644-116">Gibt den Namen des zu erstellenden Tresors an.</span><span class="sxs-lookup"><span data-stu-id="f9644-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="f9644-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9644-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9644-118">Gibt den Namen der Azure-Ressourcengruppe an, in der das angegebene Recovery Services-Objekt erstellt oder aus der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9644-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="f9644-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9644-119">-Tag</span></span>

<span data-ttu-id="f9644-120">Gibt die Tags an, die dem Tresor für Wiederherstellungsdienste hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f9644-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9644-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9644-121">-Confirm</span></span>
<span data-ttu-id="f9644-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9644-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9644-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9644-123">-WhatIf</span></span>
<span data-ttu-id="f9644-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9644-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9644-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9644-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9644-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9644-126">CommonParameters</span></span>
<span data-ttu-id="f9644-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9644-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9644-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9644-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9644-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9644-129">INPUTS</span></span>

### <span data-ttu-id="f9644-130">Keine</span><span class="sxs-lookup"><span data-stu-id="f9644-130">None</span></span>

## <span data-ttu-id="f9644-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9644-131">OUTPUTS</span></span>

### <span data-ttu-id="f9644-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="f9644-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f9644-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f9644-133">NOTES</span></span>

## <span data-ttu-id="f9644-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f9644-134">RELATED LINKS</span></span>

[<span data-ttu-id="f9644-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f9644-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="f9644-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f9644-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="f9644-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f9644-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


