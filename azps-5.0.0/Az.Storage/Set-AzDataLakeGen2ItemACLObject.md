---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175987"
---
# <span data-ttu-id="fa862-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="fa862-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="fa862-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa862-102">SYNOPSIS</span></span>
<span data-ttu-id="fa862-103">Erstellt/aktualisiert ein datalake-Gen2-Element-ACL-Objekt, das in Update-AzDataLakeGen2Item-Cmdlet verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa862-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="fa862-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa862-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="fa862-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa862-105">DESCRIPTION</span></span>
<span data-ttu-id="fa862-106">Das Cmdlet " **Satz-AzDataLakeGen2ItemAclObject** " erstellt/aktualisiert ein datalake Gen2-Element-ACL-Objekt, das in Update-AzDataLakeGen2Item-Cmdlet verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa862-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="fa862-107">Wenn der neue ACL-Eintrag mit dem gleichen AccessControlType/Entity-DefaultScope nicht in der Eingabe-ACL vorhanden ist, wird ein neuer ACL-Eintrag erstellt, ansonsten Update-Berechtigung für vorhandenen ACL-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="fa862-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="fa862-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa862-108">EXAMPLES</span></span>

### <span data-ttu-id="fa862-109">Beispiel 1: Erstellen eines ACL-Objekts mit 3 ACL-Eintrag und Update-ACL für ein Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="fa862-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="fa862-110">Dieser Befehl erstellt ein ACL-Objekt mit 3 ACL-Einträgen (Use-Inputobject-Parameter zum Hinzufügen von ACL-Einträgen zu einem vorhandenen ACL-Objekt) und aktualisiert die ACL für ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="fa862-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="fa862-111">Beispiel 2: Erstellen eines ACL-Objekts mit 4 ACL-Einträgen und Aktualisieren der Berechtigung eines vorhandenen ACL-Eintrags</span><span class="sxs-lookup"><span data-stu-id="fa862-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

<span data-ttu-id="fa862-112">Dieser Befehl erstellt zunächst ein ACL-Objekt mit 4 ACL-Einträgen und führt dann das Cmdlet erneut mit unterschiedlicher Berechtigung, aber demselben AccessControlType/Entitäts-DefaultScope eines vorhandenen ACL-Eintrags aus.</span><span class="sxs-lookup"><span data-stu-id="fa862-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="fa862-113">Dann wird die Berechtigung des ACL-Eintrags aktualisiert, aber es wird kein neuer ACL-Eintrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fa862-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="fa862-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa862-114">PARAMETERS</span></span>

### <span data-ttu-id="fa862-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="fa862-115">-AccessControlType</span></span>
<span data-ttu-id="fa862-116">Es gibt vier Arten: "Benutzer" gewährt dem Besitzer oder einem benannten Benutzerrechte, "Gruppe" gewährt Rechte für die besitzende Gruppe oder eine benannte Gruppe, "Maske" schränkt die Rechte ein, die für benannte Benutzer und die Mitglieder von Gruppen gewährt werden, und "Other" gewährt Rechte an alle Benutzer, die in keinem der anderen Einträge gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="fa862-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa862-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="fa862-117">-DefaultScope</span></span>
<span data-ttu-id="fa862-118">Legen Sie diesen Parameter fest, um anzugeben, dass der ACE zur Standard-ACL für ein Verzeichnis gehört; Andernfalls ist Scope implizit und der ACE gehört zur Access-ACL.</span><span class="sxs-lookup"><span data-stu-id="fa862-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa862-119">-Entitäts-Nr</span><span class="sxs-lookup"><span data-stu-id="fa862-119">-EntityId</span></span>
<span data-ttu-id="fa862-120">Der Bezeichner des Benutzers oder der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fa862-120">The user or group identifier.</span></span>
<span data-ttu-id="fa862-121">Sie wird bei Einträgen von AccessControlType "Maske" und "Other" ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="fa862-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="fa862-122">Der Benutzer-oder Gruppenbezeichner wird auch für den Besitzer und die besitzende Gruppe ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="fa862-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="fa862-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fa862-123">-InputObject</span></span>
<span data-ttu-id="fa862-124">Wenn das PSPathAccessControlEntry \[ \] -Objekt eingegeben wird, wird die neue ACL als neues Element des Eingabe PSPathAccessControlEntry-Objekts hinzugefügt \[ \] .</span><span class="sxs-lookup"><span data-stu-id="fa862-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa862-125">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="fa862-125">-Permission</span></span>
<span data-ttu-id="fa862-126">Das Feld "Berechtigung" ist eine 3-Zeichen-Sequenz, in der das erste Zeichen "r" ist, um Lesezugriff zu gewähren, das zweite Zeichen "w", um Schreibzugriff zu gewähren, und das dritte Zeichen "x", um die EXECUTE-Berechtigung zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="fa862-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="fa862-127">Wenn Access nicht gewährt wird, wird das Zeichen "-" verwendet, um zu kennzeichnen, dass die Berechtigung verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="fa862-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="fa862-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa862-128">CommonParameters</span></span>
<span data-ttu-id="fa862-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa862-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa862-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa862-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa862-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa862-131">INPUTS</span></span>

### <span data-ttu-id="fa862-132">Keine</span><span class="sxs-lookup"><span data-stu-id="fa862-132">None</span></span>

## <span data-ttu-id="fa862-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa862-133">OUTPUTS</span></span>

### <span data-ttu-id="fa862-134">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="fa862-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="fa862-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa862-135">NOTES</span></span>

## <span data-ttu-id="fa862-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa862-136">RELATED LINKS</span></span>
