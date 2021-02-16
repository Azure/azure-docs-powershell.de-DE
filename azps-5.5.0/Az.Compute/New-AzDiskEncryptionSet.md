---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148868"
---
# <span data-ttu-id="7a371-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7a371-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="7a371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a371-102">SYNOPSIS</span></span>
<span data-ttu-id="7a371-103">Erstellt einen Datenträgerverschlüsselungssatz.</span><span class="sxs-lookup"><span data-stu-id="7a371-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="7a371-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a371-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a371-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a371-105">DESCRIPTION</span></span>
<span data-ttu-id="7a371-106">Erstellt einen Datenträgerverschlüsselungssatz.</span><span class="sxs-lookup"><span data-stu-id="7a371-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="7a371-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a371-107">EXAMPLES</span></span>

### <span data-ttu-id="7a371-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a371-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="7a371-109">Erstellt einen Datenträgerverschlüsselungssatz mit dem angegebenen aktiven Schlüssel im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7a371-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="7a371-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a371-110">PARAMETERS</span></span>

### <span data-ttu-id="7a371-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a371-111">-AsJob</span></span>
<span data-ttu-id="7a371-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7a371-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a371-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a371-113">-DefaultProfile</span></span>
<span data-ttu-id="7a371-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a371-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a371-115">-InputObject</span></span>
<span data-ttu-id="7a371-116">Das lokale Objekt des Datenträgerverschlüsselungssets.</span><span class="sxs-lookup"><span data-stu-id="7a371-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a371-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7a371-117">-Name</span></span>
<span data-ttu-id="7a371-118">Name des Datenträgerverschlüsselungssatzs.</span><span class="sxs-lookup"><span data-stu-id="7a371-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a371-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a371-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a371-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7a371-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a371-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a371-121">-Confirm</span></span>
<span data-ttu-id="7a371-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a371-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a371-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7a371-123">-WhatIf</span></span>
<span data-ttu-id="7a371-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a371-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a371-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a371-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a371-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a371-126">CommonParameters</span></span>
<span data-ttu-id="7a371-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a371-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a371-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a371-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a371-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a371-129">INPUTS</span></span>

### <span data-ttu-id="7a371-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7a371-130">System.String</span></span>

### <span data-ttu-id="7a371-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7a371-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="7a371-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a371-132">OUTPUTS</span></span>

### <span data-ttu-id="7a371-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7a371-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="7a371-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a371-134">NOTES</span></span>

## <span data-ttu-id="7a371-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a371-135">RELATED LINKS</span></span>
