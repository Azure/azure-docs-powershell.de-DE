---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458923"
---
# <span data-ttu-id="c61b8-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="c61b8-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="c61b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c61b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c61b8-103">Ruft eine Liste der Sicherungstresor für Azure NetApp Files (ANF)-Konten ab.</span><span class="sxs-lookup"><span data-stu-id="c61b8-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="c61b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c61b8-104">SYNTAX</span></span>

### <span data-ttu-id="c61b8-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c61b8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c61b8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c61b8-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c61b8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c61b8-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c61b8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c61b8-108">DESCRIPTION</span></span>
<span data-ttu-id="c61b8-109">Das **Get-AzNetAppFilesVault-Cmdlet** ruft die Liste der Sicherungstresor eines ANF-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="c61b8-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="c61b8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c61b8-110">EXAMPLES</span></span>

### <span data-ttu-id="c61b8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c61b8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="c61b8-112">Dieser Befehl ruft eine Liste der Sicherungstresor für das Azure NetappFiles (ANF)-Konto "MyAnfAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="c61b8-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="c61b8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c61b8-113">PARAMETERS</span></span>

### <span data-ttu-id="c61b8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c61b8-114">-AccountName</span></span>
<span data-ttu-id="c61b8-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="c61b8-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61b8-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="c61b8-116">-AccountObject</span></span>
<span data-ttu-id="c61b8-117">Das Konto für das neue Sicherungsobjekt</span><span class="sxs-lookup"><span data-stu-id="c61b8-117">The account for the new backup object</span></span>

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

### <span data-ttu-id="c61b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61b8-118">-DefaultProfile</span></span>
<span data-ttu-id="c61b8-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c61b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c61b8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c61b8-120">-ResourceGroupName</span></span>
<span data-ttu-id="c61b8-121">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="c61b8-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c61b8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c61b8-122">-ResourceId</span></span>
<span data-ttu-id="c61b8-123">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="c61b8-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="c61b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61b8-124">CommonParameters</span></span>
<span data-ttu-id="c61b8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c61b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61b8-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c61b8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61b8-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c61b8-127">INPUTS</span></span>

### <span data-ttu-id="c61b8-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c61b8-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="c61b8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c61b8-129">System.String</span></span>

## <span data-ttu-id="c61b8-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c61b8-130">OUTPUTS</span></span>

### <span data-ttu-id="c61b8-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="c61b8-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="c61b8-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c61b8-132">NOTES</span></span>

## <span data-ttu-id="c61b8-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c61b8-133">RELATED LINKS</span></span>
