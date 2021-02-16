---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: cdde8169c4b068b986910dc3bfc5de446833f5ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151052"
---
# <span data-ttu-id="0bdf0-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0bdf0-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="0bdf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="0bdf0-103">Aktualisiert MSI auf den Tresor der Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="0bdf0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bdf0-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bdf0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bdf0-105">DESCRIPTION</span></span>
<span data-ttu-id="0bdf0-106">Dieses Cmdlet wird zum Hinzufügen oder Entfernen der MSI aus dem Tresor der Wiederherstellungsdienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="0bdf0-107">Verwenden Sie den "-IdentityType"-Parameter, um dem RSVault eine "SystemAssigned"-Identität zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="0bdf0-108">Verwenden Sie IdentityType None, um die MSI aus dem Tresor zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="0bdf0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0bdf0-109">EXAMPLES</span></span>

### <span data-ttu-id="0bdf0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0bdf0-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="0bdf0-111">Dieses Cmdlet wird verwendet, um einem Wiederherstellungsdienstetresor eine "SystemAssigned"-Identität hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="0bdf0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bdf0-112">PARAMETERS</span></span>

### <span data-ttu-id="0bdf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bdf0-113">-DefaultProfile</span></span>
<span data-ttu-id="0bdf0-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bdf0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0bdf0-115">-Name</span></span>

<span data-ttu-id="0bdf0-116">Gibt den Namen des zu aktualisierenden Tresors der Wiederherstellungsdienste an.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-116">Specifies the name of the recovery services vault to update.</span></span>

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

### <span data-ttu-id="0bdf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bdf0-117">-ResourceGroupName</span></span>

<span data-ttu-id="0bdf0-118">Gibt den Namen der Azure-Ressourcengruppe an, in der der Tresor der Wiederherstellungsdienste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

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

### <span data-ttu-id="0bdf0-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0bdf0-119">-IdentityType</span></span>
<span data-ttu-id="0bdf0-120">Der dem Wiederherstellungsdiensttresor zugewiesene MSI-Typ.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-120">The MSI type assigned to Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0bdf0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bdf0-121">-Confirm</span></span>
<span data-ttu-id="0bdf0-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bdf0-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0bdf0-123">-WhatIf</span></span>
<span data-ttu-id="0bdf0-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bdf0-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bdf0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bdf0-126">CommonParameters</span></span>
<span data-ttu-id="0bdf0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bdf0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bdf0-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bdf0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bdf0-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0bdf0-129">INPUTS</span></span>

### <span data-ttu-id="0bdf0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0bdf0-130">System.String</span></span>

## <span data-ttu-id="0bdf0-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0bdf0-131">OUTPUTS</span></span>

### <span data-ttu-id="0bdf0-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span><span class="sxs-lookup"><span data-stu-id="0bdf0-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="0bdf0-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0bdf0-133">NOTES</span></span>

## <span data-ttu-id="0bdf0-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0bdf0-134">RELATED LINKS</span></span>
