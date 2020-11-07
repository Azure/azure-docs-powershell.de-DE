---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: d2a379567ab96f5776b55c4cfbac2eabeaeb02a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845028"
---
# <span data-ttu-id="0ebf7-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0ebf7-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="0ebf7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ebf7-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebf7-103">Aktualisiert ein Azure NetApp-Dateien (ANF)-Konto mit der neuen Datengruppe.</span><span class="sxs-lookup"><span data-stu-id="0ebf7-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="0ebf7-104">Nützlich zum Löschen von zugehörigen aktiven Verzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="0ebf7-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="0ebf7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ebf7-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ebf7-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ebf7-106">DESCRIPTION</span></span>
<span data-ttu-id="0ebf7-107">Das Cmdlet " **Satz-AzNetAppFilesAccount** " ändert ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="0ebf7-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="0ebf7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ebf7-108">EXAMPLES</span></span>

### <span data-ttu-id="0ebf7-109">Beispiel 1: Ändern eines ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="0ebf7-109">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="0ebf7-110">Dieser Befehl führt eine Aktualisierung des angegebenen Kontos durch.</span><span class="sxs-lookup"><span data-stu-id="0ebf7-110">This command performs an update on the given account.</span></span> <span data-ttu-id="0ebf7-111">Das Fehlen des Active Directory bedeutet, dass es aus dem Konto entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="0ebf7-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="0ebf7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ebf7-112">PARAMETERS</span></span>

### <span data-ttu-id="0ebf7-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="0ebf7-113">-ActiveDirectories</span></span>
<span data-ttu-id="0ebf7-114">Ein Hashtable-Array, das die aktiven Verzeichnisse darstellt</span><span class="sxs-lookup"><span data-stu-id="0ebf7-114">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebf7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebf7-115">-DefaultProfile</span></span>
<span data-ttu-id="0ebf7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ebf7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ebf7-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="0ebf7-117">-Location</span></span>
<span data-ttu-id="0ebf7-118">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="0ebf7-118">The location of the resource</span></span>

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

### <span data-ttu-id="0ebf7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0ebf7-119">-Name</span></span>
<span data-ttu-id="0ebf7-120">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="0ebf7-120">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebf7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ebf7-121">-ResourceGroupName</span></span>
<span data-ttu-id="0ebf7-122">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="0ebf7-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="0ebf7-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ebf7-123">-Tag</span></span>
<span data-ttu-id="0ebf7-124">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="0ebf7-124">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="0ebf7-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ebf7-125">-Confirm</span></span>
<span data-ttu-id="0ebf7-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ebf7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ebf7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ebf7-127">-WhatIf</span></span>
<span data-ttu-id="0ebf7-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ebf7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ebf7-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ebf7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ebf7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebf7-130">CommonParameters</span></span>
<span data-ttu-id="0ebf7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebf7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0ebf7-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebf7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebf7-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ebf7-133">INPUTS</span></span>

### <span data-ttu-id="0ebf7-134">Keine</span><span class="sxs-lookup"><span data-stu-id="0ebf7-134">None</span></span>

## <span data-ttu-id="0ebf7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ebf7-135">OUTPUTS</span></span>

### <span data-ttu-id="0ebf7-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0ebf7-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="0ebf7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ebf7-137">NOTES</span></span>

## <span data-ttu-id="0ebf7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ebf7-138">RELATED LINKS</span></span>
