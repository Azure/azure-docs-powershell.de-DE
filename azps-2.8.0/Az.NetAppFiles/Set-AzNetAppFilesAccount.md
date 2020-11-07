---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: 873b506ea1fd50e2869a19a45a302c5fe12a781b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822580"
---
# <span data-ttu-id="dbf5c-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="dbf5c-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="dbf5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbf5c-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf5c-103">Aktualisiert ein Azure NetApp-Dateien (ANF)-Konto mit der neuen Datengruppe.</span><span class="sxs-lookup"><span data-stu-id="dbf5c-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="dbf5c-104">Nützlich zum Löschen von zugehörigen aktiven Verzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="dbf5c-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="dbf5c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbf5c-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf5c-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbf5c-106">DESCRIPTION</span></span>
<span data-ttu-id="dbf5c-107">Das Cmdlet " **Satz-AzNetAppFilesAccount** " ändert ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="dbf5c-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="dbf5c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbf5c-108">EXAMPLES</span></span>

### <span data-ttu-id="dbf5c-109">Beispiel 1: Ändern eines ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="dbf5c-109">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="dbf5c-110">Dieser Befehl führt eine Aktualisierung des angegebenen Kontos durch.</span><span class="sxs-lookup"><span data-stu-id="dbf5c-110">This command performs an update on the given account.</span></span> <span data-ttu-id="dbf5c-111">Das Fehlen des Active Directory bedeutet, dass es aus dem Konto entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="dbf5c-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="dbf5c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbf5c-112">PARAMETERS</span></span>

### <span data-ttu-id="dbf5c-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="dbf5c-113">-ActiveDirectories</span></span>
<span data-ttu-id="dbf5c-114">Ein Hashtable-Array, das die aktiven Verzeichnisse darstellt</span><span class="sxs-lookup"><span data-stu-id="dbf5c-114">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="dbf5c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf5c-115">-DefaultProfile</span></span>
<span data-ttu-id="dbf5c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbf5c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf5c-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="dbf5c-117">-Location</span></span>
<span data-ttu-id="dbf5c-118">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="dbf5c-118">The location of the resource</span></span>

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

### <span data-ttu-id="dbf5c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dbf5c-119">-Name</span></span>
<span data-ttu-id="dbf5c-120">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="dbf5c-120">The name of the ANF account</span></span>

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

### <span data-ttu-id="dbf5c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf5c-121">-ResourceGroupName</span></span>
<span data-ttu-id="dbf5c-122">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="dbf5c-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="dbf5c-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="dbf5c-123">-Tag</span></span>
<span data-ttu-id="dbf5c-124">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="dbf5c-124">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="dbf5c-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbf5c-125">-Confirm</span></span>
<span data-ttu-id="dbf5c-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbf5c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf5c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf5c-127">-WhatIf</span></span>
<span data-ttu-id="dbf5c-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbf5c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf5c-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbf5c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf5c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf5c-130">CommonParameters</span></span>
<span data-ttu-id="dbf5c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf5c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dbf5c-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbf5c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf5c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbf5c-133">INPUTS</span></span>

### <span data-ttu-id="dbf5c-134">Keine</span><span class="sxs-lookup"><span data-stu-id="dbf5c-134">None</span></span>

## <span data-ttu-id="dbf5c-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbf5c-135">OUTPUTS</span></span>

### <span data-ttu-id="dbf5c-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="dbf5c-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="dbf5c-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbf5c-137">NOTES</span></span>

## <span data-ttu-id="dbf5c-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbf5c-138">RELATED LINKS</span></span>
