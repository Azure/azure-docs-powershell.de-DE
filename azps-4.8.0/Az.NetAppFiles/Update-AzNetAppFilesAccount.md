---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 621d4d29d061566e894617d5e918440ba531a041
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166483"
---
# <span data-ttu-id="bb063-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bb063-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="bb063-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb063-102">SYNOPSIS</span></span>
<span data-ttu-id="bb063-103">Aktualisiert ein Azure NetApp-Dateien (ANF)-Konto gemäß den bereitgestellten optionalen Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="bb063-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="bb063-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb063-104">SYNTAX</span></span>

### <span data-ttu-id="bb063-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb063-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb063-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb063-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb063-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb063-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb063-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb063-108">DESCRIPTION</span></span>
<span data-ttu-id="bb063-109">Das Cmdlet **Update-AzNetAppFilesAccount** ändert ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="bb063-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="bb063-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb063-110">EXAMPLES</span></span>

### <span data-ttu-id="bb063-111">Beispiel 1: Aktualisieren eines ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="bb063-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="bb063-112">Dieser Befehl führt eine Aktualisierung des angegebenen Kontos durch, in dem die Tags entsprechend geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bb063-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="bb063-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb063-113">PARAMETERS</span></span>

### <span data-ttu-id="bb063-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="bb063-114">-ActiveDirectory</span></span>
<span data-ttu-id="bb063-115">Ein Hashtable-Array, das die aktiven Verzeichnisse darstellt</span><span class="sxs-lookup"><span data-stu-id="bb063-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb063-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb063-116">-DefaultProfile</span></span>
<span data-ttu-id="bb063-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bb063-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb063-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb063-118">-InputObject</span></span>
<span data-ttu-id="bb063-119">Das zu aktualisierende Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="bb063-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb063-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="bb063-120">-Location</span></span>
<span data-ttu-id="bb063-121">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="bb063-121">The location of the resource</span></span>

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

### <span data-ttu-id="bb063-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bb063-122">-Name</span></span>
<span data-ttu-id="bb063-123">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="bb063-123">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb063-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb063-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb063-125">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="bb063-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="bb063-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bb063-126">-ResourceId</span></span>
<span data-ttu-id="bb063-127">Die Ressourcen-ID des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="bb063-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="bb063-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="bb063-128">-Tag</span></span>
<span data-ttu-id="bb063-129">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="bb063-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="bb063-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bb063-130">-Confirm</span></span>
<span data-ttu-id="bb063-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb063-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb063-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb063-132">-WhatIf</span></span>
<span data-ttu-id="bb063-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb063-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb063-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb063-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb063-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb063-135">CommonParameters</span></span>
<span data-ttu-id="bb063-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb063-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb063-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb063-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb063-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb063-138">INPUTS</span></span>

### <span data-ttu-id="bb063-139">Keine</span><span class="sxs-lookup"><span data-stu-id="bb063-139">None</span></span>

## <span data-ttu-id="bb063-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb063-140">OUTPUTS</span></span>

### <span data-ttu-id="bb063-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bb063-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="bb063-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb063-142">NOTES</span></span>

## <span data-ttu-id="bb063-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb063-143">RELATED LINKS</span></span>
