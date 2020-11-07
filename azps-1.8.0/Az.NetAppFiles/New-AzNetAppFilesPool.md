---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: fdadfde6c798bf404d1f99dbb1ff2a8109d41f73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660981"
---
# <span data-ttu-id="c1a12-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c1a12-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="c1a12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1a12-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a12-103">Erstellt einen neuen Azure NetApp-Dateien (ANF)-Pool.</span><span class="sxs-lookup"><span data-stu-id="c1a12-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="c1a12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1a12-104">SYNTAX</span></span>

### <span data-ttu-id="c1a12-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1a12-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a12-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1a12-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1a12-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1a12-107">DESCRIPTION</span></span>
<span data-ttu-id="c1a12-108">Das Cmdlet **New-AzNetAppFilesPool** erstellt einen ANF-Pool.</span><span class="sxs-lookup"><span data-stu-id="c1a12-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="c1a12-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1a12-109">EXAMPLES</span></span>

### <span data-ttu-id="c1a12-110">Beispiel 1: Erstellen eines ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="c1a12-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="c1a12-111">Dieser Befehl erstellt den neuen ANF-Pool "MyAnfPool" innerhalb des Kontos "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="c1a12-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="c1a12-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1a12-112">PARAMETERS</span></span>

### <span data-ttu-id="c1a12-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="c1a12-113">-AccountName</span></span>
<span data-ttu-id="c1a12-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="c1a12-114">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a12-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="c1a12-115">-AccountObject</span></span>
<span data-ttu-id="c1a12-116">Das Konto für das neue Pool Objekt</span><span class="sxs-lookup"><span data-stu-id="c1a12-116">The account for the new pool object</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a12-117">-DefaultProfile</span></span>
<span data-ttu-id="c1a12-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1a12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1a12-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="c1a12-119">-Location</span></span>
<span data-ttu-id="c1a12-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="c1a12-120">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a12-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c1a12-121">-Name</span></span>
<span data-ttu-id="c1a12-122">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="c1a12-122">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a12-123">-Pools</span><span class="sxs-lookup"><span data-stu-id="c1a12-123">-PoolSize</span></span>
<span data-ttu-id="c1a12-124">Die Größe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="c1a12-124">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a12-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a12-125">-ResourceGroupName</span></span>
<span data-ttu-id="c1a12-126">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="c1a12-126">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a12-127">-Service Level</span><span class="sxs-lookup"><span data-stu-id="c1a12-127">-ServiceLevel</span></span>
<span data-ttu-id="c1a12-128">Die Dienstebene des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="c1a12-128">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="c1a12-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1a12-129">-Tag</span></span>
<span data-ttu-id="c1a12-130">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="c1a12-130">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a12-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1a12-131">-Confirm</span></span>
<span data-ttu-id="c1a12-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1a12-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1a12-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1a12-133">-WhatIf</span></span>
<span data-ttu-id="c1a12-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1a12-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1a12-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1a12-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1a12-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a12-136">CommonParameters</span></span>
<span data-ttu-id="c1a12-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a12-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c1a12-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1a12-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a12-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1a12-139">INPUTS</span></span>

### <span data-ttu-id="c1a12-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c1a12-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="c1a12-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1a12-141">OUTPUTS</span></span>

### <span data-ttu-id="c1a12-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c1a12-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c1a12-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1a12-143">NOTES</span></span>

## <span data-ttu-id="c1a12-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1a12-144">RELATED LINKS</span></span>
