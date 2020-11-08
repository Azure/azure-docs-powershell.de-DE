---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009163"
---
# <span data-ttu-id="2befe-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2befe-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="2befe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2befe-102">SYNOPSIS</span></span>
<span data-ttu-id="2befe-103">Aktualisiert ein Azure NetApp-Dateien (ANF)-Konto mit der neuen Datengruppe.</span><span class="sxs-lookup"><span data-stu-id="2befe-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="2befe-104">Nützlich zum Löschen von zugehörigen aktiven Verzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="2befe-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="2befe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2befe-105">SYNTAX</span></span>

### <span data-ttu-id="2befe-106">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2befe-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2befe-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="2befe-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2befe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2befe-108">DESCRIPTION</span></span>
<span data-ttu-id="2befe-109">Das Cmdlet " **Satz-AzNetAppFilesAccount** " ändert ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="2befe-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="2befe-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2befe-110">EXAMPLES</span></span>

### <span data-ttu-id="2befe-111">Beispiel 1: Ändern eines ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="2befe-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="2befe-112">Dieser Befehl führt eine Aktualisierung des angegebenen Kontos durch.</span><span class="sxs-lookup"><span data-stu-id="2befe-112">This command performs an update on the given account.</span></span> <span data-ttu-id="2befe-113">Das Fehlen des Active Directory bedeutet, dass es aus dem Konto entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2befe-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="2befe-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2befe-114">PARAMETERS</span></span>

### <span data-ttu-id="2befe-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="2befe-115">-ActiveDirectory</span></span>
<span data-ttu-id="2befe-116">Ein Hashtable-Array, das die aktiven Verzeichnisse darstellt</span><span class="sxs-lookup"><span data-stu-id="2befe-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2befe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2befe-117">-DefaultProfile</span></span>
<span data-ttu-id="2befe-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2befe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2befe-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="2befe-119">-Location</span></span>
<span data-ttu-id="2befe-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="2befe-120">The location of the resource</span></span>

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

### <span data-ttu-id="2befe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2befe-121">-Name</span></span>
<span data-ttu-id="2befe-122">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="2befe-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="2befe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2befe-123">-ResourceGroupName</span></span>
<span data-ttu-id="2befe-124">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="2befe-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="2befe-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2befe-125">-Tag</span></span>
<span data-ttu-id="2befe-126">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="2befe-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="2befe-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2befe-127">-Confirm</span></span>
<span data-ttu-id="2befe-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2befe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2befe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2befe-129">-WhatIf</span></span>
<span data-ttu-id="2befe-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2befe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2befe-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2befe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2befe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2befe-132">CommonParameters</span></span>
<span data-ttu-id="2befe-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2befe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2befe-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2befe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2befe-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2befe-135">INPUTS</span></span>

### <span data-ttu-id="2befe-136">Keine</span><span class="sxs-lookup"><span data-stu-id="2befe-136">None</span></span>

## <span data-ttu-id="2befe-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2befe-137">OUTPUTS</span></span>

### <span data-ttu-id="2befe-138">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2befe-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="2befe-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="2befe-139">NOTES</span></span>

## <span data-ttu-id="2befe-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2befe-140">RELATED LINKS</span></span>
