---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168553"
---
# <span data-ttu-id="d442d-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d442d-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="d442d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d442d-102">SYNOPSIS</span></span>
<span data-ttu-id="d442d-103">Ruft die Objektreplikationsrichtlinie eines Speicherkontos ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="d442d-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="d442d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d442d-104">SYNTAX</span></span>

### <span data-ttu-id="d442d-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d442d-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d442d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d442d-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d442d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d442d-107">DESCRIPTION</span></span>
<span data-ttu-id="d442d-108">Das **Cmdlet "Get-AzStorageObjectReplicationPolicy"** ruft die Objektreplikationsrichtlinie eines Speicherkontos ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="d442d-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="d442d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d442d-109">EXAMPLES</span></span>

### <span data-ttu-id="d442d-110">Beispiel 1: Sie können eine Objektreplikationsrichtlinie mit einer bestimmten Richtlinien-ID erhalten und deren Regeln anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d442d-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
```
PS C:\> $policy = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId 56bfa11c-81ef-4f8d-b307-5e5386e16fba

PS C:\> $policy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> $policy.Rules

RuleId                               SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------                               --------------- -------------------- ------------------- -----------------------
d3d39a01-8d92-40e5-849f-e56209ae5cf5 src1            dest1                {}                                         
2407de9a-3301-4656-858f-359d185565e0 src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="d442d-111">Dieser Befehl ruft eine Objektreplikationsrichtlinie mit einer bestimmten Richtlinien-ID ab und zeigt deren Regeln an.</span><span class="sxs-lookup"><span data-stu-id="d442d-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="d442d-112">Beispiel 2: Auflisten der Objektreplikationsrichtlinie aus einem Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="d442d-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="d442d-113">Dieser Befehl listet die Objektreplikationsrichtlinie aus einem Speicherkonto auf.</span><span class="sxs-lookup"><span data-stu-id="d442d-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="d442d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d442d-114">PARAMETERS</span></span>

### <span data-ttu-id="d442d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d442d-115">-DefaultProfile</span></span>
<span data-ttu-id="d442d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d442d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d442d-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="d442d-117">-PolicyId</span></span>
<span data-ttu-id="d442d-118">Id der Objektreplikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d442d-118">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d442d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d442d-119">-ResourceGroupName</span></span>
<span data-ttu-id="d442d-120">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d442d-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d442d-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d442d-121">-StorageAccount</span></span>
<span data-ttu-id="d442d-122">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="d442d-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d442d-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d442d-123">-StorageAccountName</span></span>
<span data-ttu-id="d442d-124">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="d442d-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d442d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d442d-125">CommonParameters</span></span>
<span data-ttu-id="d442d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d442d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d442d-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d442d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d442d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d442d-128">INPUTS</span></span>

### <span data-ttu-id="d442d-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d442d-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d442d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d442d-130">OUTPUTS</span></span>

### <span data-ttu-id="d442d-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d442d-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="d442d-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d442d-132">NOTES</span></span>

## <span data-ttu-id="d442d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d442d-133">RELATED LINKS</span></span>
