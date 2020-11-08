---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: f3b1a6180fb59b3c44942459e09a22a333fc9720
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177804"
---
# <span data-ttu-id="6934b-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6934b-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="6934b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6934b-102">SYNOPSIS</span></span>
<span data-ttu-id="6934b-103">Erstellt einen neuen Azure NetApp-Dateien (ANF)-Pool.</span><span class="sxs-lookup"><span data-stu-id="6934b-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="6934b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6934b-104">SYNTAX</span></span>

### <span data-ttu-id="6934b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6934b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6934b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6934b-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6934b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6934b-107">DESCRIPTION</span></span>
<span data-ttu-id="6934b-108">Das Cmdlet **New-AzNetAppFilesPool** erstellt einen ANF-Pool.</span><span class="sxs-lookup"><span data-stu-id="6934b-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="6934b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6934b-109">EXAMPLES</span></span>

### <span data-ttu-id="6934b-110">Beispiel 1: Erstellen eines ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="6934b-110">Example 1: Create an ANF pool</span></span>
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

<span data-ttu-id="6934b-111">Dieser Befehl erstellt den neuen ANF-Pool "MyAnfPool" innerhalb des Kontos "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="6934b-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="6934b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6934b-112">PARAMETERS</span></span>

### <span data-ttu-id="6934b-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="6934b-113">-AccountName</span></span>
<span data-ttu-id="6934b-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="6934b-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="6934b-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="6934b-115">-AccountObject</span></span>
<span data-ttu-id="6934b-116">Das Konto für das neue Pool Objekt</span><span class="sxs-lookup"><span data-stu-id="6934b-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="6934b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6934b-117">-DefaultProfile</span></span>
<span data-ttu-id="6934b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6934b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6934b-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="6934b-119">-Location</span></span>
<span data-ttu-id="6934b-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="6934b-120">The location of the resource</span></span>

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

### <span data-ttu-id="6934b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6934b-121">-Name</span></span>
<span data-ttu-id="6934b-122">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="6934b-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6934b-123">-Pools</span><span class="sxs-lookup"><span data-stu-id="6934b-123">-PoolSize</span></span>
<span data-ttu-id="6934b-124">Die Größe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="6934b-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6934b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6934b-125">-ResourceGroupName</span></span>
<span data-ttu-id="6934b-126">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="6934b-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="6934b-127">-Service Level</span><span class="sxs-lookup"><span data-stu-id="6934b-127">-ServiceLevel</span></span>
<span data-ttu-id="6934b-128">Die Dienstebene des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="6934b-128">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="6934b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="6934b-129">-Tag</span></span>
<span data-ttu-id="6934b-130">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="6934b-130">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6934b-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6934b-131">-Confirm</span></span>
<span data-ttu-id="6934b-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6934b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6934b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6934b-133">-WhatIf</span></span>
<span data-ttu-id="6934b-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6934b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6934b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6934b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6934b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6934b-136">CommonParameters</span></span>
<span data-ttu-id="6934b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6934b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6934b-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6934b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6934b-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6934b-139">INPUTS</span></span>

### <span data-ttu-id="6934b-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6934b-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="6934b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6934b-141">OUTPUTS</span></span>

### <span data-ttu-id="6934b-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6934b-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="6934b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="6934b-143">NOTES</span></span>

## <span data-ttu-id="6934b-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6934b-144">RELATED LINKS</span></span>
