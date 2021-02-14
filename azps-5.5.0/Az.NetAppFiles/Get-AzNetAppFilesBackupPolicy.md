---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 754149172b3154975580a0802426f9a2f20c0f62
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154508"
---
# <span data-ttu-id="54f63-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="54f63-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="54f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54f63-102">SYNOPSIS</span></span>
<span data-ttu-id="54f63-103">Ruft Details zu einer Azure NetApp Files (ANF)-Sicherungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="54f63-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="54f63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54f63-104">SYNTAX</span></span>

### <span data-ttu-id="54f63-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="54f63-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54f63-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f63-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54f63-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f63-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54f63-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54f63-108">DESCRIPTION</span></span>
<span data-ttu-id="54f63-109">Das **Cmdlet "Get-AzNetAppFilesBackupPolicy"** ruft Details einer ANF-Sicherungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="54f63-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="54f63-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54f63-110">EXAMPLES</span></span>

### <span data-ttu-id="54f63-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54f63-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="54f63-112">Dieser Befehl ruft die Sicherungsrichtlinie mit dem Namen "MyBackupPolicy" für das Konto "MyAnfAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="54f63-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="54f63-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54f63-113">PARAMETERS</span></span>

### <span data-ttu-id="54f63-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54f63-114">-AccountName</span></span>
<span data-ttu-id="54f63-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="54f63-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f63-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="54f63-116">-AccountObject</span></span>
<span data-ttu-id="54f63-117">Das Kontoobjekt mit der zurückzukehrenden Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="54f63-117">The Account object containing the Backup Policy to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54f63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f63-118">-DefaultProfile</span></span>
<span data-ttu-id="54f63-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54f63-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54f63-120">-Name</span><span class="sxs-lookup"><span data-stu-id="54f63-120">-Name</span></span>
<span data-ttu-id="54f63-121">Der Name der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="54f63-121">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f63-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f63-122">-ResourceGroupName</span></span>
<span data-ttu-id="54f63-123">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="54f63-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f63-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54f63-124">-ResourceId</span></span>
<span data-ttu-id="54f63-125">Die Ressourcen-ID der ANF-Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="54f63-125">The resource id of the ANF Backup Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f63-126">CommonParameters</span></span>
<span data-ttu-id="54f63-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f63-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54f63-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f63-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54f63-129">INPUTS</span></span>

### <span data-ttu-id="54f63-130">System.String</span><span class="sxs-lookup"><span data-stu-id="54f63-130">System.String</span></span>

### <span data-ttu-id="54f63-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="54f63-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="54f63-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54f63-132">OUTPUTS</span></span>

### <span data-ttu-id="54f63-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="54f63-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="54f63-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54f63-134">NOTES</span></span>

## <span data-ttu-id="54f63-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54f63-135">RELATED LINKS</span></span>
