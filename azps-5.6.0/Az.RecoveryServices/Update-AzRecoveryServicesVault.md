---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: 104bb05b4a01f5407c56e6c89de632a1ec5ab475
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927616"
---
# <span data-ttu-id="3d238-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3d238-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="3d238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d238-102">SYNOPSIS</span></span>
<span data-ttu-id="3d238-103">Aktualisiert MSI für den Wiederherstellungsdienste-Tresor.</span><span class="sxs-lookup"><span data-stu-id="3d238-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="3d238-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d238-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d238-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d238-105">DESCRIPTION</span></span>
<span data-ttu-id="3d238-106">Dieses Cmdlet wird zum Hinzufügen oder Entfernen des MSI aus dem Wiederherstellungsdienste-Tresor verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d238-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="3d238-107">Verwenden Sie -IdentityType-Param, um dem RSVault eine SystemAssigned-Identität zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="3d238-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="3d238-108">Verwenden Sie IdentityType None, um den MSI aus dem Tresor zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="3d238-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="3d238-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d238-109">EXAMPLES</span></span>

### <span data-ttu-id="3d238-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d238-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="3d238-111">Dieses Cmdlet wird verwendet, um einem Wiederherstellungsdienstetresor eine SystemAssigned-Identität hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3d238-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="3d238-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3d238-112">PARAMETERS</span></span>

### <span data-ttu-id="3d238-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d238-113">-DefaultProfile</span></span>
<span data-ttu-id="3d238-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d238-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d238-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3d238-115">-Name</span></span>

<span data-ttu-id="3d238-116">Gibt den Namen des zu aktualisierenden Wiederherstellungsdienste-Tresors an.</span><span class="sxs-lookup"><span data-stu-id="3d238-116">Specifies the name of the recovery services vault to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d238-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d238-117">-ResourceGroupName</span></span>

<span data-ttu-id="3d238-118">Gibt den Namen der Azure-Ressourcengruppe an, in der der Wiederherstellungsdiensttresor vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3d238-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d238-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3d238-119">-IdentityType</span></span>
<span data-ttu-id="3d238-120">Der dem Wiederherstellungsdienste-Tresor zugewiesene MSI-Typ.</span><span class="sxs-lookup"><span data-stu-id="3d238-120">The MSI type assigned to Recovery Services Vault.</span></span>

```yaml
Type: MSIdentity
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d238-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d238-121">-Confirm</span></span>
<span data-ttu-id="3d238-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d238-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d238-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d238-123">-WhatIf</span></span>
<span data-ttu-id="3d238-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d238-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d238-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d238-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d238-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d238-126">CommonParameters</span></span>
<span data-ttu-id="3d238-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d238-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d238-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d238-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d238-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d238-129">INPUTS</span></span>

### <span data-ttu-id="3d238-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3d238-130">System.String</span></span>

## <span data-ttu-id="3d238-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d238-131">OUTPUTS</span></span>

### <span data-ttu-id="3d238-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span><span class="sxs-lookup"><span data-stu-id="3d238-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="3d238-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3d238-133">NOTES</span></span>

## <span data-ttu-id="3d238-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3d238-134">RELATED LINKS</span></span>
