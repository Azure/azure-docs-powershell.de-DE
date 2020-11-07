---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 87febe648a845d595f35c1a14b024fbd97824be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660982"
---
# <span data-ttu-id="78daf-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="78daf-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="78daf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78daf-102">SYNOPSIS</span></span>
<span data-ttu-id="78daf-103">Erstellt ein neues Azure NetApp-Dateien (ANF)-Konto.</span><span class="sxs-lookup"><span data-stu-id="78daf-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="78daf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78daf-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78daf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78daf-105">DESCRIPTION</span></span>
<span data-ttu-id="78daf-106">Das Cmdlet **New-AzNetAppFilesAccount** erstellt ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="78daf-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="78daf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78daf-107">EXAMPLES</span></span>

### <span data-ttu-id="78daf-108">Beispiel 1: Erstellen eines ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="78daf-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="78daf-109">Mit diesem Befehl wird das neue ANF-Konto "MyAnfAccount" erstellt.</span><span class="sxs-lookup"><span data-stu-id="78daf-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="78daf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="78daf-110">PARAMETERS</span></span>

### <span data-ttu-id="78daf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78daf-111">-DefaultProfile</span></span>
<span data-ttu-id="78daf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78daf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78daf-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="78daf-113">-Location</span></span>
<span data-ttu-id="78daf-114">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="78daf-114">The location of the resource</span></span>

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

### <span data-ttu-id="78daf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="78daf-115">-Name</span></span>
<span data-ttu-id="78daf-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="78daf-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="78daf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78daf-117">-ResourceGroupName</span></span>
<span data-ttu-id="78daf-118">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="78daf-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="78daf-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="78daf-119">-Tag</span></span>
<span data-ttu-id="78daf-120">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="78daf-120">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="78daf-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78daf-121">-Confirm</span></span>
<span data-ttu-id="78daf-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78daf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78daf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78daf-123">-WhatIf</span></span>
<span data-ttu-id="78daf-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78daf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78daf-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78daf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78daf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78daf-126">CommonParameters</span></span>
<span data-ttu-id="78daf-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78daf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="78daf-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78daf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78daf-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78daf-129">INPUTS</span></span>

### <span data-ttu-id="78daf-130">Keine</span><span class="sxs-lookup"><span data-stu-id="78daf-130">None</span></span>

## <span data-ttu-id="78daf-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78daf-131">OUTPUTS</span></span>

### <span data-ttu-id="78daf-132">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="78daf-132">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="78daf-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="78daf-133">NOTES</span></span>

## <span data-ttu-id="78daf-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78daf-134">RELATED LINKS</span></span>
