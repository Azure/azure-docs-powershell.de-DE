---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009742"
---
# <span data-ttu-id="742e3-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="742e3-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="742e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="742e3-102">SYNOPSIS</span></span>
<span data-ttu-id="742e3-103">Erstellt ein neues Azure NetApp-Dateien (ANF)-Konto.</span><span class="sxs-lookup"><span data-stu-id="742e3-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="742e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="742e3-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="742e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="742e3-105">DESCRIPTION</span></span>
<span data-ttu-id="742e3-106">Das Cmdlet **New-AzNetAppFilesAccount** erstellt ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="742e3-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="742e3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="742e3-107">EXAMPLES</span></span>

### <span data-ttu-id="742e3-108">Beispiel 1: Erstellen eines ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="742e3-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="742e3-109">Mit diesem Befehl wird das neue ANF-Konto "MyAnfAccount" erstellt.</span><span class="sxs-lookup"><span data-stu-id="742e3-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="742e3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="742e3-110">PARAMETERS</span></span>

### <span data-ttu-id="742e3-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="742e3-111">-ActiveDirectory</span></span>
<span data-ttu-id="742e3-112">Ein Hashtable-Array, das die aktiven Verzeichnisse darstellt</span><span class="sxs-lookup"><span data-stu-id="742e3-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="742e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742e3-113">-DefaultProfile</span></span>
<span data-ttu-id="742e3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="742e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="742e3-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="742e3-115">-Location</span></span>
<span data-ttu-id="742e3-116">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="742e3-116">The location of the resource</span></span>

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

### <span data-ttu-id="742e3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="742e3-117">-Name</span></span>
<span data-ttu-id="742e3-118">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="742e3-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="742e3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742e3-119">-ResourceGroupName</span></span>
<span data-ttu-id="742e3-120">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="742e3-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="742e3-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="742e3-121">-Tag</span></span>
<span data-ttu-id="742e3-122">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="742e3-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="742e3-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="742e3-123">-Confirm</span></span>
<span data-ttu-id="742e3-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="742e3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="742e3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="742e3-125">-WhatIf</span></span>
<span data-ttu-id="742e3-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="742e3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="742e3-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="742e3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="742e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742e3-128">CommonParameters</span></span>
<span data-ttu-id="742e3-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742e3-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="742e3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742e3-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="742e3-131">INPUTS</span></span>

### <span data-ttu-id="742e3-132">Keine</span><span class="sxs-lookup"><span data-stu-id="742e3-132">None</span></span>

## <span data-ttu-id="742e3-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="742e3-133">OUTPUTS</span></span>

### <span data-ttu-id="742e3-134">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="742e3-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="742e3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="742e3-135">NOTES</span></span>

## <span data-ttu-id="742e3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="742e3-136">RELATED LINKS</span></span>
